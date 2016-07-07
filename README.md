# Part4-GoogleSheets-gRPCAPI-Adapter-Script-Docker  

The docker compose runs two containers:  
grpc container which runs the Google Grpc server and responsible for sharing the main.proto file using volumes and the other localhost container which runs the adapter server on tomcat.
