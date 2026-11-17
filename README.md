# Spring Security JWT

REST API project developed in Java using Spring Boot 3, Spring Security 6 for JWT Authentication and Authorization, and H2 database.

## Features

- Token-based Authentication using JSON Web Token (JWT)
- Role-based authorization
- Encoding password with BCrypt algorithm

## Requirements

- Java 17
- Spring Boot 3.x.x
- Spring Security 6.x.x
- Apache Maven 3.8.6

## Libraries

- [spring-common-parent](https://github.com/erebelo/spring-common-parent): Manages the Spring Boot version and provide common configurations for plugins and formatting.

## Configuring Maven for GitHub Dependencies

To pull the `spring-common-parent` dependency, follow these steps:

1. **Generate a Personal Access Token**:

   Go to your GitHub account -> **Settings** -> **Developer settings** -> **Personal access tokens** -> **Tokens (classic)** -> **Generate new token (classic)**:

    - Fill out the **Note** field: `Pull packages`.
    - Set the scope:
        - `read:packages` (to download packages)
    - Click **Generate token**.

2. **Set Up Maven Authentication**:

   In your local Maven `settings.xml`, define the GitHub repository authentication using the following structure:

   ```xml
   <servers>
     <server>
       <id>github-spring-common-parent</id>
       <username>USERNAME</username>
       <password>TOKEN</password>
     </server>
   </servers>
   ```

   **NOTE**: Replace `USERNAME` with your GitHub username and `TOKEN` with the personal access token you just generated.

## Run App

- Set the following environment variables: `DB_PASSWORD`, `ADMIN_PASSWORD` and `SECRET_KEY` (size >= 256 bits).
- Run the `SpringSecurityJwtApplication` class as Java Application.

## Collection

[Project Collection](https://github.com/erebelo/spring-security-jwt/tree/main/collection)

## AWS Demo

[Spring Security JWT](https://jwt.erebelo.com/spring-security-jwt/swagger-ui/index.html)

## AWS Deployment

Follow the [AWS Docker](https://github.com/erebelo/aws-docker/tree/main) guide to deploy a **Java App** instance and how to set up **Nginx** as a reverse proxy with a valid Wildcard SSL/TLS certificate.
