# spring3-security
This is a Spring Boot project with Spring Web Security

### Example requests
#### GET request with a authentication header
curl --location --request GET 'localhost:8080/api/v1/demo' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ6YXJhZ296YUBtYWlsLmNvbSIsImlhdCI6MTY3MzEwNjk2MywiZXhwIjoxNjczMTA4NDAzfQ.GqKrMGF4lWavV8YTM5W2gX33bhxPFxim30R8qTFyKB8'

#### POST to register and get a jwt token
curl --location --request POST 'localhost:8080/api/v1/auth/register' \
--header 'Content-Type: application/json' \
--data-raw '{
    "firstname": "Ricardo",
    "lastname": "Zaragoza",
    "email": "zaragoza@mail.com",
    "password": "zaragoza"
}'

#### POST to authenticate and get a token based with the email and password of the user
curl --location --request POST 'localhost:8080/api/v1/auth/authenticate' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "zaragoza@mail.com",
    "password": "zaragoza"
}'
