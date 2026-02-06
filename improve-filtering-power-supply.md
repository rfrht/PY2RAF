# Improving the filtering of a 600W 13.8V power supply

## Specifying the PSU
I was in need of a beefy 13.8V power supply (PSU) for my new linear amplifier. After evaluating the cost x benefit x needs, I bought a [MeanWell LRS-600-15](https://www.meanwell.com/webapp/product/search.aspx?prod=LRS-600) from [DigiKey](https://www.digikey.com/en/products/detail/mean-well-usa-inc/LRS-600-15/16394231). The 15V variant provides a 13.8V output at the trim-pot in fully counter-clockwise (minimum adjustable voltage) position and 600W maximum power output, resulting in 43 amperes at 13.8 volts. That's a bit too close to the maximum power needs of my amplifier (on specs, peak 40 A), but considering the SSB as my preferential mode and lighter duty cycle, I'm sticking to this model. No plans to do FT8 (as of now, grins).

## The elephant in the room - switching noise
While I picked a reputable manufacturer (MeanWell), these low cost switched power supplies are known for leaking the switcher noise into the downstream regulated output. The PSU [datasheet](https://www.meanwell.com/webapp/product/search.aspx?prod=LRS-600) specified a maximum 200 mVpp ripple, and a oscillator frequency (fosc) from 50-130 kHz.

These findings were measured on a Rigol DS1054Z, channel 1, AC coupled, bandwidth limited to 20 MHz (as per the spec tests). Upon powering up the PSU without any load, this is what I found at the power terminals:

![](https://github.com/user-attachments/assets/d886c270-eee8-42ef-9861-72e91c79207a)

Delving deeper in the artifacts, this is the first and stronger artifact:

![](https://github.com/user-attachments/assets/0de4ccaa-475a-4db7-87f4-5670c79b14e2)

Using the cursor functionality, it identified an approx. 140 mVpp noise with fundamental frequency at ~ 370 kHz. 370 kHz is "radio active." Its harmonics extend much further up into the spectrum, quickly reaching the amateur radio frequencies. Now, let's look at the sine'ish artifact:

 ![](https://github.com/user-attachments/assets/83999694-f111-45ef-9a23-83960b459d8c)

Here we can see a ~ 715 kHz noise at ~ 28 mVpp, hinting a first harmonic of the fundamental 370 kHz noise.

## Proposed Resolution
A Google Gemini session suggested that since I'm using a high current (50A) power supply, it is harder to use off-the-shelf "EMI Filters" (which are usually rated for only 3–10 Amps).

The AI suggested building a Low-Pass Filter using capacitors. Since 370 kHz is a high frequency, it will need a mix of capacitor types:

* **1x Electrolytic Capacitor:** 2200µF to 4700µF (25V or 35V).
    * *Role:* Absorbs the "slow" energy and stabilizes voltage.
    * *Crucial Spec:* It must be "Low ESR" (Equivalent Series Resistance). Standard "general purpose" caps are too slow to catch 370 kHz noise. Look for brands like Panasonic (FR/FM series), Rubycon (ZLH), or Nichicon.

* **2x Ceramic Capacitors (High Speed):** 0.1µF (100nF) and 1µF (X7R type).
    * *Role:* These act like a short-circuit for high-frequency noise (370kHz - 714kHz). Electrolytics are "blind" to these fast frequencies; ceramics catch them.
 
* **1x large Ferrite:** Material 75 ferrite.
    * *Role:* Some of the noise might be Common Mode (noise on both wires relative to earth). Thus, suggested adding a ferrite. Because the current goes out on V+ and back on V-, the magnetic fields cancel out, so the core doesn't saturate. It only blocks the noise that is common to both lines.
    * *Crucial Spec:* Get a large **Material 75** Ferrite Ring (Toroid) or clip-on. Just slapping unknown/random material ferrites will not necessarily yield good results. [I tested with a Material 46 clip-on](https://github.com/user-attachments/assets/ed62b839-2b92-4374-a05e-30fbe72713b0) and the noise went happily through it. Ferrite material **matters**.
    * *Technique:* Pass BOTH the V+ and V- wires through the ring together, **near the device**. Wrap them around the ring 2-3 times if they fit.


## Bill of materials
- [Rubycon ZLR series, electrolytic low ESR 3300 µF, 25V](https://www.digikey.com/en/products/detail/rubycon/25ZLR3300MEFC12-5X35/25271325)
- [Ceramic capacitor, X7R, 0.1 µF, 50V](https://www.digikey.com/en/products/detail/kemet/C320C104K5R5TA7305/12701231)
- [Ceramic capacitor, X7R, 1 µF, 50V](https://www.digikey.com/en/products/detail/kemet/C420C105K5R5TA7200/18120556)
- [Clip-on Fair-Rite Material 75 ferrite](https://www.digikey.com/en/products/detail/fair-rite-products-corp/0475164181/8594151)

## How to Install
* Mount the capacitors **directly at the power input terminals of your device** (*not at the PSU end*). This forces the noise to travel down the wire (which acts as a resistor/inductor) and get some attenuation before hitting your capacitor "wall".
* Wind one or more turns of the power supply cable in the ferrite, near the device (not at the PSU end).
* Twist your wires tightly (approx 1 twist per inch).

This is how I assembled together all the capacitors:

![](https://github.com/user-attachments/assets/e4c379aa-19c9-432e-a75f-83f5fd258e9b)

## Results
After installing the capacitors _inside_ my amplifier, the larger 370 kHz ripple was wiped off entirely:

![](https://github.com/user-attachments/assets/e3060783-215d-4c36-907b-19479ebe4cd0)

While somewhat attenuated (from ~ 28 mVpp to ~22 mVpp), there was a remaining ~ 714 kHz ripple though:

![](https://github.com/user-attachments/assets/054744ea-25cc-48ea-ab39-02159703c030)

Then I wound 1 turn of the PSU cable in a Material 75 clip-on ferrite:

![](https://github.com/user-attachments/assets/8ead735d-c774-4570-9641-fc56e3ddec35)

Which choked big time the remaining ripple:

![](https://github.com/user-attachments/assets/df368208-32f1-4bbb-9e4f-2b803b963018)

Resulting in a transformed and meager 11 mVpp ripple at 285 kHz. (Note: This 285 kHz signal is likely a harmless resonance artifact from the filter itself, known as 'tank circuit ringing,' and is negligible compared to the original noise.)

# Conclusion
With ~ $15 worth of parts I was able to transform transform a somewhat noisy PSU into a unit with **<12mV ripple**, surpassing the noise floor of many linear supplies and beating the Alinco DM-330MV (58mV) by a factor of five.

Quick recap. It was:

![](https://github.com/user-attachments/assets/d886c270-eee8-42ef-9861-72e91c79207a)

It ended as:

![](https://github.com/user-attachments/assets/94aa1be7-6c50-4d82-9560-f54cd1df2298)

Hope this helps - 73 de PY2RAF.
