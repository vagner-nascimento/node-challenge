# node-challenge
A node JS challenge to evaluate the developer skills

# pre requirements
 - NodeJS and NPM
 - Docker and Docker Compose

# requirements
  - Must be used pure Javascript(ECMA6), Typescript and other languages will be declassified
  - Responses and requests data should be in JSON format
  - Create a GET HTTP route on "/live" path that returns: Status 200 - Body: { "status": "OK" }
  - Subscribe into "thing" queue to receive data events to process. The payload is on "data" folder
  - Call rest mock on "http://localhots:4000/type/{id}" passing the "type_id" of the original payload and add "type_name" field to the original data, with "name" received from the call. If data is not found or some error occurs on the call, this field should be null.
  - Publish the enriched data into "animals" queue
  
  # infra
  - All required infra (rabbit server and rest mock) can be found into docker/compose-infra.yml
  - Run this command from root folder to initialize whole infra: docker-compose -f ./docker-infra.yml up --build
  - Rabbit MQ connection string: amqp://guest:guest@localhost:5672
  - To access rabbit management panel access http://localhost:15672/ (user: guest, pass: guest)
  - GET url to see all available data into rest mock: http://localhots:4000/db
  - The data of rest mock is into docker/mocks/rest/db.json