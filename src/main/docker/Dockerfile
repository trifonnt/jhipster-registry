FROM fabric8/java-alpine-openjdk8-jdk

# add directly the war
ADD *.war /deployments/jhipster-registry.war

VOLUME /tmp

# --spring.cloud.config.server.git.uri=${GIT_URI} --spring.cloud.config.server.git.search-paths=${GIT_SEARCH_PATHS}

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTIONS="-Djava.security.egd=file:/dev/./urandom" \
    JAVA_MAX_MEM_RATIO=90 \
    JAVA_APP_DIR=/deployments \
    JAVA_APP_JAR=jhipster-registry.war \
    SPRING_PROFILES_ACTIVE=prod,git \
    SPRING_CLOUD_CONFIG_SERVER_GIT_URI=https://github.com/trifonnt/jhipster-registry-sample-config/ \
    SPRING_CLOUD_CONFIG_SERVER_GIT_SEARCH-PATH=central-config

EXPOSE 8761
