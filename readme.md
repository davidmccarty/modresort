# MOD RESORTS
This is a sample program forked from IBM.  
It runs a simple web page from a liberty server

## Build
```sh
mvn clean package
docker build -t modresort .
docker tag modresort:latest davidmccarty/modresort:1.0.0
docker push davidmccarty/modresort:1.0.0
```

## Run locally
```sh
docker run -p 9080:9080 davidmccarty/modresort:1.0.0
```
Then access using   
http://localhost:9080/resorts  
http://localhost:9080/metrics

## Customize
Optional weather 

