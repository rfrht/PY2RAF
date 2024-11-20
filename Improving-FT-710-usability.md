# Improving the out-of-box FT-710 usability

## WIP (Work in Progress)

When I first got my radio, **of course** I didn't read the manual and I went to operate it immediately. Few nuisances showed up, and for some picky operators, this is how I addressed them.

## Power Meter needle
Argh, that was a killer for me. Out-of-the factory, the meter comes configured as "average" power instead of "peak" power. That resulted in a lazy needle around 30ish Watts, seldom hitting the 50s, and never the 100W. How to fix it:
1. Hit the `FUNC` button
2. Bottom row, select `OPERATION SETTING`
3. Touch `TX GENERAL`
4. Turn the `FUNC` button, scroll down to `METER DETECTOR`
5. Touch `METER DETECTOR`
6. Turn the `FUNC` button, change it to `PEAK`
7. Touch `BACK` to exit the configuration

## Frequency shift when exchanging between USB and LSB
When you switch between USB/LSB/AM/CW, you'll get a frequency shift of +- 800 Hz, and that's not super useful for me, as I have to re-tune when I change the mode.
1. Hit the `FUNC` button
2. Bottom row, select `CW SETTING`
3. Touch `MODE CW`
4. Turn the `FUNC` button, scroll down to `CW FREQ DISPLAY`
5. Touch `CW FREQ DISPLAY`
6. Turn the `FUNC` button, change it to `DIRECT FREQ`
7. Touch `BACK` to exit the configuration

## Main VFO tuning step
You will find out that the VFO and Clarifier in SSB mode tunes in 20 Hz steps in "Fine" mode. Well, I like 10 Hz steps more.
1. Hit the `FUNC` button
2. Bottom row, select `OPERATION SETTING`
3. Touch `TUNING`
4. Turn the `FUNC` button, scroll down to `SSB/CW DIAL STEP`
5. Touch `SSB/CW DIAL STEP`
6. Turn the `FUNC` button, change it to `10 Hz`
7. Touch `BACK` to exit the configuration

## Secondary tuning dial step
Out of the box, for each step in the encoder it jumps 5 kHz in the frequency. And I also like 1 kHz more.
1. Hit the `FUNC` button
2. Bottom row, select `OPERATION SETTING`
3. Touch `TUNING`
4. Turn the `FUNC` button, scroll down to `CH STEP`
5. Touch `CH STEP`
6. Turn the `FUNC` button, change it to `1 KHz`
7. Touch `BACK` to exit the configuration

## Microphone & intelligibility
I joke with my girlfriend that if you want to **ruin** an amateur radio day is telling that the audio isn't good. LOL.

I did though, found that the stock mic sounds way too heavy on the bass side with the factory-original preset TX bandpass. Narrowing it a bit will yield better intelligibility. Here's how.
1. Hit the `FUNC` button
2. Bottom row, select `RADIO SETTING`
3. Select `MODE SSB`
4. Scroll down to `TX BPF SEL`
5. Change it to `200-2800Hz`

## Mic gain, Compressor and AMC
I was trying to make sense of it with some over-the-air recording (listening through a SDR). I found that AMC is kind of a gain configuration - the least AMC, the least signal you're putting out. Fun fact: The less AMC, the more the needle swings in `COMP` mode while TXing.

These are the instructions that I got from Yaesu to configure them all. You start with **Mic Gain**, then **AMC** and then **Compressor**.

--

1. If menu settings power and audio levels are not at the default settings, either set them all to default or reset the radio. It is paramount that you have the values reverted back to factory originals, so existing configurations won't taint the configuration.
2. Ensure the radio is in USB or LSB or AM.
3. Go to menu `OPERATION SETTING` / `TX GENERAL` / `METER DETECTOR` and set it to `PEAK`.
4. Connect the radio to a dummy load.
5. Touch the meter and select `ALC`.
6. Press the FUNC knob and select `MIC GAIN`
7. Speak normally into the microphone and adjust the mic gain so the ALC indicates towards the top quarter of the ALC scale, but not into the blue part of the scale. Don’t worry if the average reading is somewhere in the middle of the white scale, just ensure you don’t drive it past the end of the white scale. For reference, my mic gain setting is at the default of 50.
9. Touch the meter and select PO. Speak into the microphone and check that you see 100 watts output, or close to it, on the power meter on the radio.                                                                                                                  Note: When the power out setting for SSB is set to 100 watts,  ALC action will start as soon a the power out hits 100 watts, so the ALC action we saw earlier also indicates the radio is putting  100 watts on your speech peaks.
10. Touch the meter and select `COMP`.
11. Press the FUNC knob and select AMC level.
12. Now speak into the microphone and observe the Compression meter. It has a slow action, and you may have to speak for a time to see a response.
13. While speaking into the microphone, reduce the `AMC` level until you see the `COMP` level rise to the 10 db mark, or close to it. My AMC setting is at 80.
14. Check the ALC still reads mid to top of the ALC scale and you still have 100 watts out.

### Notes.
* If the AMC setting is reduced excessively, you will see a reduction in ALC action, and a drop in output power, indicating there is not enough drive to push the finals to 100 watts out.
* When using  the processor, you may have to re-adjust the AMC level to bring the compression back down to 10 db.

--

Regarding compressor, I'm yet to see a huge improvement with it. So far, I wasn't able to find any audio TX difference with compressor disabled and the maximum value. Still under investigation.
