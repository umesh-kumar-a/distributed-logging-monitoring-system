# Distributed Monitoring and Microservices Framework

A distributed system framework designed to monitor, collect, and visualize logs from multiple microservices in real time.  
This project uses Kafka, Fluentd, Elasticsearch, and Kibana to build a centralized logging and monitoring pipeline similar to production-grade cloud architectures.

All components are containerized using Docker to ensure easy deployment, scalability, and reliability.

---

## Overview

In distributed systems, logs are scattered across multiple services, making debugging and monitoring difficult.  
This framework centralizes logs and events from different services into a single monitoring stack.

The system:

- Streams logs and events through Kafka  
- Aggregates logs using Fluentd  
- Stores and indexes logs in Elasticsearch  
- Visualizes logs and metrics using Kibana  
- Monitors service heartbeat to detect failures  

This architecture closely resembles real-world observability stacks used in industry.

---

## Features

- Real-time log and event streaming with Kafka  
- Log aggregation and forwarding using Fluentd  
- Centralized storage and fast search using Elasticsearch  
- Interactive dashboards and visualization using Kibana  
- Sample microservices (inventory, order, payment)  
- Heartbeat monitoring and anomaly detection  
- Fully containerized deployment with Docker  
- Easily scalable and extendable architecture  

---

## Tech Stack

- Python  
- Apache Kafka  
- Fluentd  
- Elasticsearch  
- Kibana  
- Docker and Docker Compose  

---

## Requirements

- Docker  
- Docker Compose  
- Python 3.10 or later  

---

## Installation

Clone the repository:

git clone https://github.com/umesh-kumar-a/distributed-logging-monitoring-system.git  
cd distributed-logging-monitoring-system

Install dependencies for local development:

pip install -r requirements.txt

---

## Setup and Usage

### Start Docker Containers

Start all infrastructure services:

docker-compose up -d

This will automatically start:

- Kafka  
- Fluentd  
- Elasticsearch  
- Kibana  

---

### Run Monitoring System

Start the monitoring service to track heartbeats and logs:

python run_monitoring.py

---

### Run a Microservice

Launch any microservice:

python run_service.py <service_name>

Examples:

python run_service.py inventory_service  
python run_service.py order_service  
python run_service.py payment_service  

Each service continuously generates logs that are streamed and monitored in real time.

---

## Visualization

Open Kibana to explore logs and dashboards:

http://localhost:5601

You can:

- Search logs  
- Filter events  
- Monitor system health  
- Analyze errors  
- Visualize metrics  

---

## Project Structure
├── README.md
├── config/
├── core/
├── microservices/
├── fluentd/
├── docker-compose.yml
├── requirements.txt
├── run_monitoring.py
├── run_service.py
├── utils/

---

## Extending the System

To add a new microservice:

1. Create a new file inside the microservices folder (for example, new_service.py)  
2. Use base_service.py as a template  
3. Implement your service logic  
4. Run:

python run_service.py new_service

---

## Troubleshooting

Check running containers:

docker ps

View container logs:

docker logs <container_name>

If logs are not visible, verify Fluentd and Elasticsearch services are running properly.

---

## Learning Outcomes

This project demonstrates:

- Distributed system design  
- Centralized logging architecture  
- Real-time streaming pipelines  
- Observability and monitoring concepts  
- Docker-based deployment  
- Microservices communication  

---

