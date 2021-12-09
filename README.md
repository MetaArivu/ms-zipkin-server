# ZIPKIN SERVER

Zipkin is a distributed tracing system. It helps gather timing data needed to troubleshoot latency problems in service architectures. Features include both the collection and lookup of this data.

## Download Zipkin 
curl -sSL https://zipkin.io/quickstart.sh | bash -s


## RUN Locally
java -jar zipkin.jar

## Build and Push Docker Using Jar
- Build Docker Images 
    - docker build -t metamagic/msk8-zipkin:1.0 .
- Run Docker Image
    - docker run -p 9411:9411 metamagic/msk8-zipkin:1.0
- Push Docker Image
    - docker image push metamagic/msk8-zipkin:1.0



## Microservice Request Tracing

As all our service are Sleuth enabled, it will generate traceid and send to Zipkin.

## Demo

- Generate some request on User, Product Review and Product Service
- Screenshot showing trace-id 
- <img width="1674" alt="Screen Shot 2021-12-06 at 12 29 00 PM" src="https://user-images.githubusercontent.com/23295769/144801747-25ae8140-5e08-4d2c-a29b-9ea8b5113397.png">
- Screenshot showing request to Product -> Product Review Service
- <img width="1675" alt="Screen Shot 2021-12-06 at 12 32 02 PM" src="https://user-images.githubusercontent.com/23295769/144802003-3030575e-87b9-4532-a01c-2d654c064586.png">
- <img width="1680" alt="Screen Shot 2021-12-06 at 12 32 08 PM" src="https://user-images.githubusercontent.com/23295769/144801995-973a9254-5ab6-480f-bdc5-bb10cdec8a22.png">

