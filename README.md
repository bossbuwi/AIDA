# AIDA

### Project Details

**Framework:** [Spring Boot](https://spring.io/projects/spring-boot) version 2.6.0-RC1  
**Status:** Active - Ongoing  
**Last Release Date:** None  
**Latest Version:** None  
**Author:** [bossbuwi](https://github.com/bossbuwi)

***

### Environment Setup

**Tools Needed:**
* Java IDE, preferably [IntelliJ IDEA](https://www.jetbrains.com/idea/)
* [PostgreSQL](https://www.postgresql.org/download/) installation, version used for this project is PostgreSQL 13. pgAdmin must be included in the installation

**Setting Up for Development**
1. Connect to the postgres installation using pgAdmin. If this is your first time connecting to postgres, it will prompt you to set a master password. **Do not forget this password!** For safety reasons, you may use _admin_ as the master password for it to not be forgotten.
2. On the left hand side, there is a list of servers. A default server usually named _Postgres_ is automatically created. Connect to it. Again, if this is your first time connecting to the server, it will prompt you to set a password. **Do not forget this password!** For safety reasons, you may use _admin_ as the master password for it to not be forgotten.
3. Right click the server's _Databases_ group, then _Create > Database.._
4. Enter the following details below on the _General_ tab.
    - Database: db_aida
    - Owner: postgres (this is automatically created)
5. Go to the _Security_ tab and add a _Priviledge_ by clicking the "+" sign on the _Priviledges_ group. Enter the following details for the priviledge.
    - Grantee: postgres
    - Priviledges: tick the checkbox beside _All_
    - Grantor: postgres
6. Go to the _SQL_ tab. The statement shown should at least be close to the statement below.  
  `CREATE DATABASE db_aida`  
    `WITH`  
    `OWNER = postgres`  
    `ENCODING = 'UTF8'`  
    `CONNECTION LIMIT = -1;`  
  `GRANT ALL ON DATABASE db_aida TO postgres;`  
7. Click _Save_ to finish the database creation. A new database, _db\_aida_, should now be visible on the _Databases_ group.
