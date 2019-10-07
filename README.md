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

```curl -XPUT -H "Content-Type: application/json" localhost:9200/_bulk --data-binary @movies_elastic.json```


