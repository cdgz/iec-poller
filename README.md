Description
-----------
[IEC Canada](http://www.cic.gc.ca/english/work/iec/apply.asp?country=fr&cat=wh) website poller,
used to check "Quota", "Places" and "Status" fields for category "Working Holidays" (wh),
country France (fr). Also, [KOMPASS](https://kompass-iec-eic.international.gc.ca/iecRegistrationClosed-eicInscriptionsFermees?regionCode=FR) website checked.

Usage:

    ./poll

Returns 0 if there is no free places. To be inserted in any available 24/365 machine:

- RPi at your home
- spare [CI](http://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software) instance at work
- "free" 2-months [DO](https://www.digitalocean.com/help/referral-program/) VM

Tips
----

To get notified in time, the best solution is [Telegram bots](https://telegram.org/blog/bot-revolution). 
You can also use services like [pushover](http://pushover.net) or [pushbullet](http://pushbullet.com).
They both have free 7-day trials, which should be enough for hot period.

If you use 2nd hosting option (CI instance), check out [ngrok](http://ngrok.com)
service to escape corporate firewall. Just do:

    ngrok -log=stdout $JENKINS_PORT > /dev/null &

on Jenkins node and bookmark the URL on smartphone. Now you are free to go home and able to
correct job parameters (or disable it) remotely
