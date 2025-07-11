# RabbitMQ
docker run -d --hostname rabbit-host --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management
# ms sql
version: '3.8'

services:
  sqlserver:
    image: mcr.microsoft.com/mssql/server:2022-latest
    container_name: sqlserver
    ports:
      - "1433:1433"
    environment:
      SA_PASSWORD: "ZAQ!2wsxcde3"
      ACCEPT_EULA: "Y"
    volumes:
      - sqlserver_data:/var/opt/mssql

volumes:
  sqlserver_data:
