Description
-----------
[IEC Canada](http://www.cic.gc.ca/english/work/iec/apply.asp?country=fr&cat=wh) website poller,
used to check "Quota", "Places" and "Status" fields for category "Working Holidays" (wh),
country France (fr). Also, [KOMPASS](https://kompass-iec-eic.international.gc.ca/iecRegistrationClosed-eicInscriptionsFermees?regionCode=FR) website checked.

Usage:

    ./poll

Returns 0 if there is no free places. To be inserted in any available 24/365 machine:

- RPi at your home
- spare Jenkins slave at work
- "free" 2-months [DO](https://www.digitalocean.com/help/referral-program/) VM
