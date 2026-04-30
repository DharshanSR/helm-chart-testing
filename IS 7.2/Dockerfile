# Use your personal WSO2 IS image from Docker Hub
FROM jhon348/dharshan:7.2.0-alpha

# build arguments for external artifacts
ARG MYSQL_CONNECTOR_VERSION=8.0.30

# add MySQL JDBC connector to server home as a third party library
ADD --chown=wso2carbon:wso2 https://repo1.maven.org/maven2/mysql/mysql-connector-java/${MYSQL_CONNECTOR_VERSION}/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}.jar ${WSO2_SERVER_HOME}/repository/components/dropins/
