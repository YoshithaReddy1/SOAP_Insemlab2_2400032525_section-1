# Service Layer Dependency Mocking Demo

A minimal Spring Boot project that tests `UserController` with a mocked `UserService`.
The controller test does not require a database.

## Run the test

From the project root (the directory containing `pom.xml`):

```bash
mvn test
```

Expected: one test, zero failures, `BUILD SUCCESS`.

## Endpoint tested

`GET /users/1`

The test configures the mocked service to return:

```json
{"id": 1, "name": "Yoshitha"}
```

The test verifies HTTP 200 and the JSON fields.
