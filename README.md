# Query log analysis demo

[Query log analysis – using logstash, elasticsearch and kibana](http://nhhagen.wordpress.com/2013/11/28/query-log-analysis-using-logstash-elasticsearch-and-kibana/)

## Running the box

1. Install [Vagrant](http://www.vagrantup.com/)
2. `vagrant up`
3. Open http://localhost:5601/
4. Select a dashboard from the Kibana menu.

## Adding more data

To add more data you need to add the index template in elasticsearch/index-temaplate.json for instructions see the elasticsearch documentation.

First log into the box

    vagrant ssh

then you can run the logstash indexer-shipper.conf

    java -jar /home/vagrant/logstash/logstash.jar agent -f '/vagrant/logstash/indexer-shipper.conf'

