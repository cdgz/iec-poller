#! /bin/sh

QUOTA=`curl -s http://www.cic.gc.ca/english/work/iec/data.xml | grep -A 4 'location="France" category="wh"' | grep "<quota>0</quota>"`
PLACES=`curl -s http://www.cic.gc.ca/english/work/iec/data.xml | grep -A 4 'location="France" category="wh"' | grep "<places>0</places>"`
STATUS=`curl -s http://www.cic.gc.ca/english/work/iec/data.xml | grep -A 4 'location="France" category="wh"' | grep "<status>This category is now closed.</status>"`
KOMPASS=`curl -s "https://kompass-iec-eic.international.gc.ca/iecRegistrationClosed-eicInscriptionsFermees?regionCode=FR" | grep "The 2014 International Experience Canada (IEC) initiative with France is currently closed, and will re-open shortly.  We encourage you to check the updates on our website regularly"`

if [ ! QUOTA ] || [ ! PLACES ] || [ ! STATUS ] || [ ! KOMPASS ]; then
    exit 1;
fi
