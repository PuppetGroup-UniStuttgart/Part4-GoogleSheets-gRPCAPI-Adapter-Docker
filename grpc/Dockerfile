FROM maven:3.3-jdk-8

# Get sources
RUN git clone --recursive https://github.com/shruthikuki/CloudLab-IAAS-UniStuttgart-Part4-gRPCGoogleSheets.git
WORKDIR /CloudLab-IAAS-UniStuttgart-Part4-gRPCGoogleSheets

COPY GrpcGoogleSheets.p12 /GrpcGoogleSheets.p12

# Run maven
RUN mvn clean package

RUN ls target
COPY main.proto /api/main.proto

WORKDIR /

VOLUME /api
CMD java -cp /CloudLab-IAAS-UniStuttgart-Part4-gRPCGoogleSheets/target/gRPCGoogleSheets-0.0.1-SNAPSHOT-jar-with-dependencies.jar cloudlab.ops.GoogleSheetsServer