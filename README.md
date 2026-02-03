# Distributed Logging and Monitoring System

A centralized logging and monitoring system designed for distributed microservices using Kafka, Fluentd, Elasticsearch, and Kibana.

## Overview
This project demonstrates how logs from multiple services can be aggregated, streamed, stored, and visualized in real time for monitoring and debugging distributed systems.

## Tech Stack
- Apache Kafka
- Fluentd
- Elasticsearch
- Kibana
- Docker & Docker Compose
- Python

## Features
- Centralized log aggregation
- Real-time streaming pipeline
- Searchable log storage
- Monitoring dashboards
- Scalable microservice design

## How to Run
```bash
docker-compose up -d
python run_monitoring.py
python run_service.py <service_name>
