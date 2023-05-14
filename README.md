# LOGSTASH CONFIGURATION TEMPLATE

Tested on SOF-ELK VM environtment. You can download SOF-ELK from this link https://github.com/philhagen/sof-elk/blob/main/VM_README.md.

Procedure:
1. Set up an ELK on a Linux machine. 
2. Clone this repository into /etc/logstash/.
3. Modify the configuration file you need in /etc/logstash/logstash-configuration-template/.
4. Create 'temp' directory in /var/lib/logstash/.
5. Execute this command:<br>
<t>\# /usr/share/logstash/bin/logstash --path.data /var/lib/logstash/temp/ -f /etc/logstash/logstash-configuration-template/\<conf file name\>
5. Compare total of the documents in the targeted Elasticsearch index and total line of the source file to verify. The total of the documents in the targeted index can be found at Kibana's Stack Management → Index Management.
6. When all of the events have been ingested to the Elasticsearch node, terminate the process by pressing Ctrl + C.
