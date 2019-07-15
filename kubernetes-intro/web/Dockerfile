FROM python:3.7-alpine
LABEL MAINTAINER="dmitriypnev@gmail.com"
COPY ./app /app 
WORKDIR /app
VOLUME ["/app"]
USER 1001:1001
EXPOSE 8000
CMD python3 -m http.server 8000
