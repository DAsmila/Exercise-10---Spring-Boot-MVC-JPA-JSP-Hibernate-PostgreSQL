# Spring Boot – Class Notes Code

| Folder | What it shows |
|---|---|
| `01-spring-boot-rest-hello` | `@RestController` – "Welcome to Spring Boot" |
| `02-spring-boot-mvc-jsp-form` | Spring Boot MVC + JSP form handling (`@Controller`, `Model`) |
| `03-spring-boot-mvc-jpa-postgresql` | Spring Boot MVC + JPA + Hibernate + JSP + PostgreSQL (Student CRUD: save & list) |

## Requirements
Java 21, Maven, (project 03 only) PostgreSQL.

## Run
```bash
cd 01-spring-boot-rest-hello          # or 02-... / 03-...
mvn spring-boot:run
```
Open http://localhost:8080/

## Project 03 – database setup
1. Create the database/table using `03-spring-boot-mvc-jpa-postgresql/schema.sql`
   (Hibernate `ddl-auto=update` can also create the table).
2. Set the password as an environment variable instead of hard-coding it:
   ```bash
   export DB_PASSWORD=your_postgres_password        # Windows: set DB_PASSWORD=...
   ```
3. Run `mvn spring-boot:run` and open http://localhost:8080/ , list at `/students`.

> Note: JSP works with `mvn spring-boot:run` / running from STS. It is not supported in an executable *jar* (`java -jar`); package as `war` if you need that.
