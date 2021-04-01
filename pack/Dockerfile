FROM openjdk:8
VOLUME /tmp
ARG JAR_FILE=target/*.zip
COPY ${JAR_FILE} zdlc.zip
RUN unzip zdlc.zip
WORKDIR /UpShift-ZDLC
RUN echo $PWD
EXPOSE 8080
ENTRYPOINT ["java", "-Dlogging.config=conf/ZDLC_log4j_conf.xml", "-Dehcache.disk.store.dir=conf/ZDLC_Cache", "-jar", "lib/upshift-zdlc.jar" ]