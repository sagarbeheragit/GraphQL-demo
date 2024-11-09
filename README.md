# Project Structure

1. Entity for Products table. Defined as Entity and given table name. Primary key is auto-generated.
2. Repository interface for Products. It extends the JPA repository so all methods are there.
3. Service - Injected the repository to call the CRUD methods. To be used by the controller.
4. Controller - Has the new  GraphQL mapping @QueryMapping and  @MutationMapping instead of the REST mapping
5. resource/schema.graphqls - This file helps identify the endpoint as graphql with path localhost:port/graphql
6. Properties:
   - Define DATASOURCE PROPERTIES for MySQL 
   - JPA SPECIFIC PROPERTIES 
   - Enabling GraphQL playground (spring.graphql.graphiql.enabled=true)

# Database
1. DB used is MySQL. I used a docker container to connect. Docker command
    - **_docker run --name db-mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=Password mysql_**.
2. The above command runs a docker container from the image and publishes the port to 3306 on host. Default DB user is root.
3. New DB created with below SQL from MySQL workbench
4. When the project runs JPA creates the table. (Product)
5. Following script to create the DB from MySQL client and use the DB before starting the APP.

   	create database testdb;
   	use testdb;
# Graphql- Playground
1. App provided tested to test Graphql. Enabled in properties file
# Use from Postman
1. Test from Postman as well 