# LOGSTASH CONFIGURATION TEMPLATE

Tested on SOF-ELK VM environtment.

Procedure:
1. Clone this repository in /etc/logstash/
2. Modify the configuration file
3. Create 'temp' directory in /var/lib/logstash/
4. Execute this command:<br>
<t>\# /usr/share/logstash/bin/logstash --path data /var/lib/logstash/temp/ -c /etc/logstash/logstash-configuration-template/\<conf file name\>
5. Compare total of the documents in the targeted Elasticsearch index and total line of the source file to verify.
6. When all of the events have been ingested to the Elasticsearch node, terminate the process with Ctrl + C.
