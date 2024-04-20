FROM debian:bookworm-slim

RUN apt update && apt upgrade

RUN apt install -y curl

RUN curl -L https://download.java.net/java/GA/jdk21.0.2/f2283984656d49d69e91c558476027ac/13/GPL/openjdk-21.0.2_linux-x64_bin.tar.gz | tar -xz -C /opt 

ENV PATH="$PATH:/opt/jdk-21.0.2/bin"

RUN curl -L https://downloads.apache.org/kafka/3.7.0/kafka_2.13-3.7.0.tgz | tar -xz -C /opt

ENV PATH="$PATH:/opt/kafka_2.13-3.7.0/bin"

RUN kafka-storage.sh format -t $(kafka-storage.sh random-uuid) -c /opt/kafka_2.13-3.7.0/config/kraft/server.properties

CMD ["kafka-server-start.sh", "/opt/kafka_2.13-3.7.0/config/kraft/server.properties"]

