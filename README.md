# elasticsearch_docker
Run elasticsearch in docker

### Pull image from docker hub 
```docker pull docker pull elasticsearch:7.4.0 ```

### Run it in port 9200
```docker run -p 9200:9200 -e "discovery.type=single-node" elasticsearch:7.4.0```

### Install curl to send request 

- ```apt update && sudo apt upgrade```
- ```sudo apt install curl```

### Example of request with a json file

```curl http://localhost:9200```
```curl -XPUT -H "Content-Type: application/json" localhost:9200/_bulk --data-binary @movies_elastic.json```


### Set up KIBANA

```docker pull kibana:7.4.1```


### Run Kibana container

```docker run --link YOUR_ELASTICSEARCH_CONTAINER_NAME_OR_ID:elasticsearch -p 5601:5601 elasticsearch:7.4.0```
It can take few minutesa

### Check if Kibana is running
http://localhost:5601
