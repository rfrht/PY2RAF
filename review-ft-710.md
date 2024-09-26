# Review: Yaesu FT-710 under the perspective of a FT-991A user. (WIP)
## Introduction
I've been a [happy FT-991A user](https://github.com/rfrht/FT-991A/wiki/Review-FT-991A) since 2019. And now... The FT-710. I started writing this review with a bit less than a month operating the FT-710. Here are my ramblings.

## Why a FT-710?
First and beforehand - because the FTDX-10 was outside my budget. It would have been it. But, why a new radio? Wasn't FT-991A good enough? Sure, it was. I'm severely limited **by the antenna and my local noise**, not the radio. However, I wanted another radio so I could operate the 991A in VHF/UHF and the new radio on HF band. Simultaneously. And I wanted a new and capable HF radio, because.

## Operating
Face it, you get used to your default rig. There's an entirely new operation paradigm in the FT-710 - and [takes time and effort to adapt](https://github.com/rfrht/PY2RAF/blob/master/Improving-FT-710-usability.md). So, no longer hundreds of config clauses under a single "Setup" block, it is now grouped on functionalities in a menu-like structure. That made sense, in my opinion.

Out of the box, the radio ships a new microphone with some function buttons on it. I'm yet to play with it, but it's a departure from the MH-31 and adds shortcuts at your fingertip. Again, to be explored in the future.

CAT-wise, it is _fairly_ compatible with the FT-991A command set on the base functionality. Don't take it for granted, and if you use scripts, test and fix it.

I miss a dedicated Clarifier/RIT button, and I wish I could configure the CLAR button to on-off, instead of toggling it through CLAR RX, CLAR TX, CLAR TX/RX and finally CLAR OFF to get it off.

I found a small bug; when the radio is on `SQUELCH - FM ONLY`, the `SQL` pin on the rear port (I use it on my [timer](https://github.com/rfrht/Yaesu-OLED-TX-Timer)) stays asserted - even when the radio receiving. I'm yet to report this bug to Yaesu.

And now, the DSP - zommmmggg the DSP. The DNR is so capable (choose the right DNR setting) to the point to actually **help** weak signals. I used the DNR on my 991A only with very strong signals. On FT-710, it helps with weak signals too. Very good.

Regards the sensitivity - I leave my RX S-Meter in a point that it swings between 0-3 S-Units. So in 40M band, with the FT-991A with a clean front-end (IPO, no attenuator) I had a S2-S3 noise floor. With the 710 - this is where it blows the 991A out of water, IPO gets me to S8-9! So yes, now I have to run it attenuated, varying between 6 and 12 dB of attenunation. Damn big ears. If I lived in a RF-silent place, it would have resulted **net new contacts** due to the **very noticeable** extra sensitivity. However, as per the opening statements, I'm limited by my antenna constraints and a metropolitan area noise floor.

(to be continued)
