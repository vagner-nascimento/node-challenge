# node-challenge
A node JS challenge to evaluate the developer skills

# pre requirements
 - NodeJS and NPM
 - Docker and Docker Compose

# requiriments
  - Must use in Javascript (ECMA6), Typescript and others will be ignored
  - All responses and data entrance should be in JSON format
  - Create Http health check route on "/live"  that returns: 200 - { "status": "OK" }
  - Subscribe in a queue to receive data events to process
  - Call another rest service using GET to obtain the data to enrich the original data
  - Publish enriched data into a queue
  - OBS: If the call to the rest to the rest service fails, it should to complete the operation without this data
  
  # infra
  - All required infra (rabbit server and rest mock) is into docker/compose-infra.yml
  - Run this command from root folder to initialize whole infra: docker-compose -f ./docker-infra.yml up --build
  - Rabbit MQ connection string: amqp://guest:guest@localhost:5672
  - To access rabbit management panel access http://localhost:15672/ (user and pass are guest)
  - Rest mock base url: http://localhots:4000
  - The data of rest mock is into docker/mocks/rest/db.json

  # OBS
- you can choose the data model that you want, but when 