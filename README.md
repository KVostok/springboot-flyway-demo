# SpringBoot + Flyway demo
Project, which demonstrate integration between db migration tool Flyway and SpringBoot framework.

# Some important parts of demo
## Migrations
Project has two migrations, which are containing in:
`src/main/resources/db.migration` - all migrations, which has project.

**V00001__Create_country_table.sql**
```mysql-sql
CREATE TABLE country (id INT, name VARCHAR(30)); 
```

**V00002__Add_test_data_to_country.sql**
```mysql-sql
-- adding test data
INSERT INTO country VALUES (1, 'Ukraine');
INSERT INTO country VALUES (2, 'Russia');
INSERT INTO country VALUES (3, 'Belorus');
```

## Properties
`src/main/resources/application.properties` - properties with data for connecting to DB.
Here is properties, which are using:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/flyway_demo_db
spring.datasource.username=root
spring.datasource.password=pw
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

