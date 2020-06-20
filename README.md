# node-challenge
A node JS challange to evaluate devs skills in Node with Javascript (ECMA6)

# requiriments
  - All response and data entrace should be in JSON fromat
  - Create 2 Http health check reoutes ( /live and /ready) that retuns only { "status": "OK" }
  - Subscribe in a queue to recieve data in JSON to process
  - Call another rest service to get its data to enrich the received data
  - Publish this the new in another topic
  - If the call to the rest to the rest service fails, it should to comcplish the operation without this data
  
  # rabbit mq
    
