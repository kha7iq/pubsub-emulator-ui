FROM google/cloud-sdk:alpine

COPY run.sh /run.sh

RUN apk --update add openjdk8-jre netcat-openbsd && \
    gcloud components install beta pubsub-emulator && \
    chmod 700 /run.sh

EXPOSE 8085

CMD /run.sh