# Use a custom WSO2 IS base image published to Docker Hub
FROM jhon348/wso2is-base:7.3.0-rc1

# Define the MySQL connector version
# (Using 9.7.0 to get the latest, which uses the new mysql-connector-j naming)
ARG MYSQL_CONNECTOR_VERSION=9.7.0

# Add MySQL JDBC connector to server home as a third-party library
ADD --chown=wso2carbon:wso2 https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/${MYSQL_CONNECTOR_VERSION}/mysql-connector-j-${MYSQL_CONNECTOR_VERSION}.jar ${WSO2_SERVER_HOME}/repository/components/dropins/
