# Food_Ordering_System_with_Kafka_Python  
This project is a scalable event-driven food ordering application built using Python and Apache Kafka. It allows users to place food orders, processes those orders, sends email notifications to customers, and maintains real-time analytics.  
Run Docker Compose to start Kafka and ZooKeeper containers:  
docker-compose up -d  
## Project Structure  
The project has the following structure:  

order_backend.py: Generates order details and sends them to the order_details Kafka topic.  
transaction.py: Listens to the order_details topic, processes orders, and sends confirmation messages to the order_confirmed topic.  
email.py: Listens to the order_confirmed topic and simulates sending email notifications to customers.  
analytics.py: Listens to the order_confirmed topic and updates analytics data.  
docker-compose.yml: Defines the Docker Compose configuration for Kafka and ZooKeeper.  
