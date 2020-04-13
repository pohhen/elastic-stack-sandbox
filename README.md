# elastic-stack-sandbox
Sandbox environment for Elasticserach 7 and extensions

All Elastic-stack images can be found from Elastic.co
- https://www.docker.elastic.co/

## Modules
- Elasticsearch 7.6.2
  - running with defaults
- Kibana 7.6.2
  - no login required
- Filebeat
  - reads the logs files
  - forwards logs to Logstash
- Logstash
  - forwards logs to Elasticsearch

### Log sources
- sampleLogFiles
  - files to read by Filebeat

## Usage
```bash
docker-compose up -d
```

### Coming soon
- log source from Nginx-container
- log source from NodeJS-container
- Heartbeat
- Elastic APM (application performance monitoring)
