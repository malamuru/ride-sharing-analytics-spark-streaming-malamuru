<h1 align="center">🚖 Real-Time Ride Sharing Analytics using Apache Spark</h1>

<h3 align="center">
Streaming Data Pipeline | Spark Structured Streaming | PySpark | Data Engineering
</h3>

<p align="center"><em>"Processing real-time ride data to generate actionable insights using scalable streaming analytics."</em></p>

---

## ✨ Overview

This project implements a **real-time analytics pipeline** for a ride-sharing platform using **Apache Spark Structured Streaming**.

It simulates live ride data, processes streaming JSON input, and performs **real-time aggregations and trend analysis**.

The project demonstrates how streaming data can be handled using **window functions, aggregation, and time-based analytics**, which are essential for modern data engineering systems.

---

## 🚀 Key Features

- 📡 Real-time data ingestion using socket streaming  
- 📥 JSON parsing into structured schema  
- 📊 Aggregation of fare and distance by driver  
- ⏰ Window-based time series analysis  
- 📈 Trend analysis using sliding windows  
- 📁 Exporting streaming results to CSV  
- 🔄 Fault tolerance using Spark checkpoints  

---

## 🧠 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Spark Streaming](https://img.shields.io/badge/Spark%20Streaming-E25A1C?style=for-the-badge)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)

---

## 📂 Project Structure
- task1.py # Real-time ingestion & parsing
- task2.py # Aggregation by driver
- task3.py # Windowed trend analysis
- data_generator.py # Simulates streaming ride data
- output/ # CSV outputs
- checkpoint/ # Streaming checkpoints


---

## 📊 Dataset Schema (Simulated)

| Field        | Description |
|--------------|------------|
| trip_id      | Unique ride ID |
| driver_id    | Driver identifier |
| distance_km  | Distance traveled |
| fare_amount  | Fare collected |
| timestamp    | Ride start time |

---

## 🔍 Analysis Performed

### 📌 Real-Time Data Ingestion
- Read streaming data from socket (`localhost:9999`)
- Parsed JSON using predefined schema  

### 📌 Driver-Level Aggregation
- Computed total fare and average distance  
- Used **sliding windows (2 minutes)**  

### 📌 Trend Analysis
- Applied **5-minute windows with 1-minute slide**  
- Calculated total fare trends over time  

---

## ⚙️ How to Run

### Step 1: Install dependencies
```bash
pip install pyspark faker

```
### Step 2: Start data generator
```bash
python data_generator.py

```
### Step 3: Run streaming tasks (in separate terminals)
```bash
python task1.py
python task2.py
python task3.py

```
## 📌 Project Highlights
- Built a real-time streaming data pipeline
- Used Spark Structured Streaming
- Applied window functions & time-based analytics
- Simulated real-world ride-sharing data
- Implemented fault-tolerant streaming (checkpointing)
