# flaskapp

Simple REST API application.

## Description

This application has to endpoint:
1. HTTP GET `API_URL/api/info`
Example:
```
{
  "env":"production",
  "hostname":"ac7402803609",
  "port":"8000"
}
```
* HTTP GET `API_URL/api/date`
Example:
```
{
  "date_time":"01/09/2021, 20:41:24",
  "day":"09","month":"01",
  "time":"20:41:24","year":"2021"
}
```

## Build container image
```
docker build -t api .
```
## Run container
By deafault application use 5000/TCP port for incoming requests.
```
docker run -p 5000:5000 --name api --rm -it api
```

Use other port e.g. 8000/TCP
```
docker run -p 8000:8000 -e PORT=8000 --name api --rm -it api
```
