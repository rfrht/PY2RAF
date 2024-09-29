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

## Mic gain, Compressor and AMG
I was trying to make sense of it with some over-the-air recording (listening through a SDR). I found that AMG is kind of a gain configuration - the least AMG, the least signal you're putting out. Fun fact: The less AMG, the more the needle swings in `COMP` mode while TXing.

Regarding compressor, I'm yet to see a huge improvement with it. So far, I wasn't able to find any audio TX difference with compressor disabled and the maximum value. Still under investigation.
