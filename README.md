# elk-logging-python
Real time analytics over logs with ELK stack

## Running elastic search with docker
1) sudo docker run --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:6.7.0

## Logstash steps 
1) Logstash configuration file should be copied to "/usr/share/logstash" directory. - "logstash-simple.conf"

2) Add the path of "logFile.txt" to the logstash configuration file.

2) sudo bin/logstash -f logstash-simple.conf --path.data /usr/share/logstash/data/1

3) create visualization in Kibana with the created index.

4) Whenever the logs in the log file get updated or appended to the previous logs, as long as the three services are running the data in elasticsearch and graphs in kibana will automatically update according to the new data

[logo]

[logo]: https://github.com/binoyyj/elk-logging-python/raw/master/kibana_visualization.png "Kibana Visualization"

