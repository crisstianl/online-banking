### Online Banking Template
**bank-web** module is the application web interface developed in Html and Javascript that helps the users query their bank sold, or register new accounts, make withdrawls, or close their accounts.   
The web interfaces fetches all data from the backend services via Ajax and Rest messages.  

**bank-api** module is the application backend services developed in Java that expose the following information through endpoints:
- /account/v1/get/{name}, accepts a path parameter and produces a json message with account info.
- /account/v1, accepts a post message, creates the account and produces 200.
- /account/v1, accepts a put message containing the account name and amount, updates the balance and produces 200. 
- /account/v1, accepts a delete message containing the account name, deletes the account from the system and produces 200.

**bank-storage** module handles all the database transactions and ensures that the information is persisted in a relational database, in this case SQLite. The data is converted to the SQL types using EclipseLink.

### Instalation
- install any Java application server (Tomcat 8.5+, Glassfish 5+, Wildfly 12+, Weblogic 10+, etc).
- copy "bank-web.war" from "online-banking/bank-web/target" into your server's deployment directory.
- copy "bank-api.war" from "online-banking/bank-api/target" into your server's deployment directory.
- copy "bank-storage.war" from "online-banking/bank-storage/target" into your server's deployment directory.
- go to http://localhost:8080/bank-web to access the web interface.

### Libraries
- Javax Servlet 3.1
- Javax Jsp 2.2
- Sun Jersey 1.1
- Fasterxml Jackson 2.9
- Junit 4.1
- Mockito 2.1
- EclipseLink 2.6
- SQLite Jdbc 3.1