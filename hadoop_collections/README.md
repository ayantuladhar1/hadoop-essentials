# Hadoop Basics to Intermediate – Learning Notes 📘

This repository contains my **beginner to intermediate learning notes on Hadoop**, written step-by-step while studying **Big Data fundamentals for Data Engineering**.

The notes cover:
- Big Data concepts
- Types of Big Data
- Hadoop architecture
- HDFS concepts
- Common Hadoop & HDFS commands
- Hands-on practice examples

---

## 📌 What is Big Data?

**Big Data** refers to datasets that are:
- Too **large**
- Too **complex**
- Too **fast-growing**

to be processed efficiently using traditional databases or single machines.

---

## 📊 Types of Big Data

Big Data is commonly classified into **three types**:

### 1️⃣ Structured Data
Data with a **fixed schema** stored in rows and columns.

**Examples:**
- Relational databases (MySQL, PostgreSQL)
- CSV files
- Tables in Hive

**Characteristics:**
- Schema is predefined
- Easy to query using SQL
- Highly organized

---

### 2️⃣ Semi-Structured Data
Data that does **not follow a rigid table structure** but still contains tags or keys.

**Examples:**
- JSON
- XML
- Avro
- Logs with key-value pairs

**Characteristics:**
- Flexible schema
- Common in APIs and event data
- Widely used in data engineering pipelines

---

### 3️⃣ Unstructured Data
Data with **no predefined structure**.

**Examples:**
- Images
- Videos
- Audio files
- Free-text documents
- Social media posts

**Characteristics:**
- Difficult to analyze directly
- Requires preprocessing or ML tools
- Large storage requirement

---

## 🚀 Why Hadoop?

Traditional systems struggle with:
- Very large data sizes
- Hardware failures
- High storage cost

**Apache Hadoop** solves this by:
- Distributing data across machines
- Automatically replicating data
- Allowing parallel processing

---

## 🧩 Hadoop Core Components

| Component | Description |
|--------|-------------|
| HDFS | Distributed storage layer |
| YARN | Resource and job manager |
| MapReduce | Batch processing engine |
| Hive | SQL layer on top of Hadoop |
| Spark | Fast, in-memory processing engine |

---

## 🗄️ What is HDFS?

**HDFS (Hadoop Distributed File System)** stores data by:
- Splitting files into large blocks
- Distributing blocks across machines
- Replicating blocks for fault tolerance

---

## 🧱 HDFS Block & Replication

- **Default block size:** 128 MB  
- **Default replication factor:** 3  

This ensures:
- High availability
- Fault tolerance
- Reliable storage

---

## 🖥️ Hadoop Cluster

A **cluster** is a group of machines working together.

| Node Type | Responsibility |
|---------|----------------|
| NameNode | Stores metadata |
| DataNode | Stores actual data |
| ResourceManager | Manages resources |
| NodeManager | Executes tasks |

---

## 🔁 HDFS vs Local File System

| Feature | Local FS | HDFS |
|------|---------|------|
| Storage | Single machine | Distributed |
| Fault tolerance | ❌ | ✅ |
| Big data support | ❌ | ✅ |

---

## 🧾 Common HDFS Commands

### List files
```bash
hdfs dfs -ls /
