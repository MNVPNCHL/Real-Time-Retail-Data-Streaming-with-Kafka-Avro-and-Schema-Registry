# Real-Time-Retail-Data-Streaming-with-Kafka-Avro-and-Schema-Registry
Engineered a real-time event streaming pipeline with Confluent Kafka and Avro, enabling schema-managed, high-throughput ingestion and consumption of retail transaction data.
## Overview
This project demonstrates a **real-time data streaming pipeline** using **Apache Kafka (Confluent Cloud)**, **Schema Registry**, **Avro serialization**, and **Python**.

It simulates a **production-grade data engineering workflow** where retail transaction data is ingested, serialized, streamed through Kafka, and consumed in real time.

---

## Architecture
```
CSV Data → Python Producer → Kafka Topic → Python Consumer
                  ↓
          Schema Registry (Avro)
```

---

## Tech Stack
- **Python**
- **Apache Kafka (Confluent Cloud)**
- **Schema Registry**
- **Avro**
- **Pandas**

---

## Dataset
The dataset contains retail transaction data with the following fields:

- Invoice  
- StockCode  
- Description  
- Quantity  
- InvoiceDate  
- Price  
- CustomerID  
- Country  

---

## Avro Schema
The Avro schema ensures **structured, consistent, and schema-driven data exchange** between producer and consumer.

**Fields included:**
- `Invoice`
- `StockCode`
- `Description`
- `Quantity`
- `InvoiceDate`
- `Price`
- `CustomerID`
- `Country`

---

## Workflow

### Producer
- Reads CSV data using Pandas  
- Converts each row into dictionary format  
- Serializes records using Avro schema  
- Publishes messages to Kafka topic `retail_data_dev`
  
### 🔹 Consumer
- Subscribes to Kafka topic  
- Retrieves schema from Schema Registry  
- Deserializes Avro messages  
- Displays records in real time  

---
