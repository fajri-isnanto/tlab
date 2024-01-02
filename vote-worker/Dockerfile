FROM  yongjhih/ubuntu-openjdk-8

RUN apt-get update -qq && apt-get install -y maven && apt-get clean

WORKDIR /code

ADD pom.xml /code/pom.xml
RUN mvn compile
RUN mvn test

# Adding source, compile and package into a fat jar
ADD src /code/src
RUN mvn package

CMD ["java", "-jar", "target/worker-jar-with-dependencies.jar"]
