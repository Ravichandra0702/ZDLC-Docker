FROM openjdk:8
VOLUME /tmp
ARG JAR_FILE=target/*.zip
COPY ${JAR_FILE} hsql.zip
RUN unzip hsql.zip
WORKDIR /upshift_zdlc_hsql/db
RUN echo $PWD
ENTRYPOINT ["java", "-cp", "lib/hsqldb.jar", "org.hsqldb.server.Server", "org.hsqldb.server.Server", "-database.0", "file:data/zdlc_file;ifexists=true" ]