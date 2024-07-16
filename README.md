### Task1

Creating a topic:

  docker exec -it <kafka_container_id> kafka-topics --create --topic dbrain --bootstrap-server localhost:9092

  ![image](https://github.com/user-attachments/assets/151b1930-15fb-4c17-aff3-e40b8cf30da0)

Producing  data to  a topic:

  docker exec -it <kafka_container_id>  kafka-console-producer  --topic quickstart-events --bootstrap-server localhost:9092

  ![image](https://github.com/user-attachments/assets/c4b63d71-28b8-47e2-b31e-131a8f253084)

Consuming data from a topic:

  docker exec -it 90c0de9bb8c9 kafka-console-consumer --from-beginning --topic quickstart-events --bootstrap-server localhost:9092

  ![image](https://github.com/user-attachments/assets/c4b63d71-28b8-47e2-b31e-131a8f253084)


### Task2

  For task 2 I created 5 containers for zookeeper,kafka,server,producer and consumer services.

  Producer scrapes the https://scrapeme.live/shop/ then produces data into the pokemon topic

  Consumer saves consumed data into db file shared in app/data volume

  Server container runs a flask server for api requests

  I also added a test.py script to test the api

  ![image](https://github.com/user-attachments/assets/0283f699-1444-49cc-9553-0861d70dcd25)

### Notes:

  I also could have seperated the database service but since it was not explicitly asked I just added a sqlite db for demonstration purposes.

  I decided using python instead of java  for kafka scripts because I scrape data using a python library I wanted to keep it consistent.

  I did not put too much emphasis on task1 because I was just executing commands from apache documentation.

  

