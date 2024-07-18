# Docker compose with Keycloak, Postgres and node-app


Token generation
Authentication
Token revocation
Introspect(Authorization)
userinfo
Client, Group, Role, User implementation
 

 ## **Steps**

 1. `docker compose up`
 2. Goto `http://localhost:8080`, keycloak admin page
 3. Create new realm addition to `master` (eg: `my-realm`) by importing the `realm-export.json` located in the root. or do the following steps
    1. Create roles `my-admin` and `my-user`.
    2. Create group `my-group` and add roles to `my-admin` and `my-user`.
 4. Create user with username `admin1` and add role `my-admin` and set password
 5. Create user with username `user1` and add role `my-user` and set password.
 6. Create user with username `super-admin` and add group `my-group` (so that this user will get all permissions of `my-admin` and `my-user` roles)
 7. Import the `Postman_collection.json` in PostMan and update the client credentials and user passwords if any.
 8. Creat token using token endpoint
 9. Request for the resource