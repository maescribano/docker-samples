# docker-samples
custom docker images collection

* elasticsearch-head-shield:

  Basic docker images including elasticsearch and plugins such as head and shield. It includes a simple elasticsearch.yml configuration for shield.

   Build command:

   ```
  $> docker build -t elasticsearch_head_shield:2.4.1 .
   ```

   Run command:

   ```
  $> docker run -d -p 9200:9200 -p 9300:9300 elasticsearch_head_shield:2.4.1
   ```

   Curl command to test shield configuration:

   ```
   curl -u elasticsearch -XGET 'http://localhost:9200/'
   ```
