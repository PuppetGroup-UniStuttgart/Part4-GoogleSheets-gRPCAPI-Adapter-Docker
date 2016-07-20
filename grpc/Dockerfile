FROM maven:3.3-jdk-8

# Get sources
RUN git clone --recursive https://github.com/shruthikuki/UniStuttgart-PuppetGroup-gRPCGoogleSheets.git
WORKDIR /UniStuttgart-PuppetGroup-gRPCGoogleSheets

COPY GrpcGoogleSheets.p12 /GrpcGoogleSheets.p12

# Run maven
RUN mvn clean package

RUN ls target
COPY main.proto /api/main.proto

WORKDIR /

VOLUME /api
CMD java -cp /UniStuttgart-PuppetGroup-gRPCGoogleSheets/target/gRPCGoogleSheets-0.0.1-SNAPSHOT-jar-with-dependencies.jar cloudlab.ops.GoogleSheetsServer
