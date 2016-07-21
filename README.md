# Part4-GoogleSheets-gRPCAPI-Adapter-Script-Docker  

The docker compose bundle runs two containers:

1. grpc container: Runs the Google Sheets gRPC Server and responsible for sharing the main.proto file using volumes 
2. localhost container: Runs the adapter server on tomcat
