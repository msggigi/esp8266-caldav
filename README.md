# esp8266-caldav
Request CALDAV calendar from ESP8266 and blink LED if you find specific appointments


To test your CALDAV server you can use curl

Example with a Nextcloud Calendar instance:
'''
curl --insecure --request REPORT -u USER -H "Content-Type: text/xml" -H "Depth: 1"  --data "<c:calendar-query xmlns:D='DAV:' xmlns:c='urn:ietf:params:xml:ns:caldav'><D:prop><c:calendar-data/></D:prop>    <c:filter> <c:comp-filter name='VCALENDAR' /></c:filter></c:calendar-query>"  https://URLSERVER/remote.php/dav/calendars/USER/default | tidy -xml -i -
'''

