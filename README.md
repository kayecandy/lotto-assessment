# Running the app (Windows)

### 1. Start MySQL Server

* Create `lotto` schema
		
```sql
CREATE SCHEMA `lotto`;
```

* Edit credentials in `application.properties` 

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/lotto?serverTimezone=UTC
spring.datasource.username=<your_mysql_username>
spring.datasource.password=<your_mysql_password>
```


### 2. Run Spring Boot

```
./mvnw spring-boot:run
```



### 3. Testing in Postman

To test app in Postman, import the Postman import files found in the `/postman` directory.

> Note: To use the **ClientAPI**, add a Request Body with a "Binary" Content-Type then select the `test.csv` file found in the root directory of the source code. You may also select your own CSV file.

![enter image description here](https://i.stack.imgur.com/kcmGT.png)

# Files

```
├── postman                             # Postman import files
│   ├── Localhost.postman_environment.json
│   └── Lotto Assessment.postman_collection.json
├── src                                 # Java source files
│   └── main
│		├── java
|		└── resources
|			└── application.properties
|                                       # Application config file
├── target                              # Java class files
├── mvnw.cmd                            # Maven executable for Windows
├── pom.xml                             # Maven config file
└── test.csv                            # Sample input CSV for Client API
```
