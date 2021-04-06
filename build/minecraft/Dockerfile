ARG JAVA_VERSION
ARG JAR_FILE

FROM ${JAVA_VERSION}

USER root

COPY ./build/minecraft/server ./bin/server
COPY ./build/minecraft/scripts ./bin/server

RUN groupadd -g 1000 minecraft
RUN useradd -u 1000 -ms /bin/bash -g minecraft minecraft

RUN chown -R minecraft.minecraft /bin/server
RUN chmod -R 755 /bin/forge

RUN chmod +x /bin/forge/start.sh

WORKDIR /bin/server

USER minecraft

CMD ["sh", "/bin/server/start.sh"]
