# Graylog-Cacti-Contentpack
Contentpack for displaying Cacti-Logs

This contentpack extracts output from cacti logs and shows some details about
host individual polling times and "u"-values.

For this to work you need to export logs towards graylog from the cacti.log
file. Best way that worked for me was with nxlog since rsyslog seemed to
drop a lot of lines parsing the cacti.log. Also, you need Cacti to log
in "MEDIUM" mode to get statstics and results logged.

Step by Step:
1. Install nxlog and adjust the nxlog.conf to your server needs
2. Adjust your logrotate depending on how much datasources your 
cacti-system is handling and rotate cacti.log accordingly (ie every 4h) -it CAN get quite big quite fast
3. Set the "Poller Logging Level" to "MEDIUM" in Cacti
4. Install content pack and adjust it to your specifics (Input-IP, stream-filter, etc.)
5. Enjoy

