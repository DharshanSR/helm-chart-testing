# WSO2 Identity Server with MySQL

This repository contains a Docker configuration for running WSO2 Identity Server with MySQL as the database backend. It extends the base WSO2 IS image by adding the MySQL JDBC connector.

## Overview

WSO2 Identity Server is a comprehensive identity and access management solution that helps secure your APIs, applications, and microservices. This configuration allows WSO2 IS to use MySQL as the database backend instead of the default H2 database, providing better performance and scalability for production environments.

## Prerequisites

- Docker and Docker Compose installed
- Basic knowledge of WSO2 Identity Server
- MySQL server instance (can be containerized or external)

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/wso2is-mysql.git
   cd wso2is-mysql
   ```

2. Build the Docker image:
   ```bash
   docker build -t wso2is-mysql:7.2.0-alpha .
   ```

3. Run the container (assuming you have a MySQL instance running):
   ```bash
   docker run -p 9443:9443 -p 9763:9763 wso2is-mysql:7.2.0-alpha
   ```

## Configuration

This Dockerfile extends the base WSO2 IS image (`jhon348/dharshan:7.2.0-alpha`) by adding the MySQL Connector/J driver version 8.0.30. 

To connect the WSO2 Identity Server to your MySQL instance, you'll need to:

1. Create a MySQL database for WSO2 IS
2. Configure the datasource in `<WSO2_IS_HOME>/repository/conf/datasources/master-datasources.xml`
3. Update any other necessary configurations

## Environment Variables

When running the container, you can provide the following environment variables:

- `MYSQL_HOST`: MySQL host address (default: localhost)
- `MYSQL_PORT`: MySQL port (default: 3306)
- `MYSQL_DATABASE`: MySQL database name
- `MYSQL_USERNAME`: MySQL username
- `MYSQL_PASSWORD`: MySQL password