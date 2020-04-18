# elastic-stack-sandbox
Sandbox environment for Elasticsearch 7 and extensions like Kibana, beats and other monitorings.

[![Build Status](https://cloud.drone.io/api/badges/pohhen/elastic-stack-sandbox/status.svg)](https://cloud.drone.io/pohhen/elastic-stack-sandbox)

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
- APM-server
  - Cathers application perfomance data from NodeJS-demo

### Log sources
- sampleLogFiles
  - files to read by Filebeat
- Nginx-demo
  - automatically sends access.log from localhost:8080 to Elasticsearch
- NodeJS-demo
  - automatically sends application performance data from localhost:3000 to Elasticsearch

## Usage
```bash
docker-compose up -d --build
```
```bash
# Just the AMP demo
docker-compose up -d --build nodejs-demo
```

### Coming soon
- Heartbeat
