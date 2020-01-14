FROM openjdk:8


COPY . .
# change to unix line endings
RUN sed -i 's/\r//' mvnw 
RUN ./mvnw package

CMD java -jar ./target/docker-example-1.1.3.jar