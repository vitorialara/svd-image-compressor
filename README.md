# 🖼️ Distributed Image Compression Pipeline (SVD + PySpark + Airflow)

This project implements a **distributed, scalable image ingestion and compression pipeline** built using **Apache Airflow** and **PySpark**. The system extracts images from multiple online sources, compresses them using **Singular Value Decomposition (SVD)**, and stores results along with metadata in **MongoDB** and **Google Cloud Storage (GCS)**. **MLflow** is used to track compression experiments and metrics.

---

## 🎯 Project Objectives

- Build a distributed, scalable ETL pipeline for processing 1M+ images
- Compress image data using **SVD** while preserving essential features
- Enable seamless **storage, retrieval, and tracking** across cloud services
- Lay groundwork for future large-scale image analytics and ML applications

---

## 🛠️ Tech Stack

| Category       | Tools Used                                  |
|----------------|----------------------------------------------|
| Workflow       | **Apache Airflow**                           |
| Distributed Processing | **PySpark**, Pandas, NumPy           |
| Compression    | **Singular Value Decomposition (SVD)**       |
| Storage        | **MongoDB**, **Google Cloud Storage (GCS)** |
| Experiment Tracking | **MLflow**                              |
| Data Sources   | Pexels, Unsplash, Wallhaven APIs             |
| Others         | Python, OpenCV, PIL                          |

---

## 🔍 Key Features

### 🧩 Distributed Image ETL
- Orchestrated using **Airflow DAGs**
- Parallel data fetching, transformation, and compression

### 🖼️ Image Compression with SVD
- Implemented custom SVD algorithm in `compression.py`
- Reduces file size while retaining image quality
- Tracks compression ratios and quality metrics via **MLflow**

### ☁️ Scalable Cloud Storage
- Compressed images pushed to **Google Cloud Storage**
- Metadata and links stored in **MongoDB** for unified querying

### 📈 ML Experiment Tracking
- Tracks SVD compression performance (e.g. reconstruction loss, rank)
- Uses **MLflow** for versioning and comparison across runs

### 📥 Source Integration
- Pulls images from:
  - Unsplash (`unsplash_play.ipynb`)
  - Pexels (`pexels_play.ipynb`)
  - Wallhaven (`wallhaven_play.ipynb`)

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/distributed-image-compression.git
cd distributed-image-compression
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure `.env` for API keys and GCS paths

### 4. Launch Airflow
```bash
airflow db init
airflow webserver --port 8080
airflow scheduler
```

### 5. Run DAG to start full ingestion + compression pipeline

---

## 📂 Notable Scripts

| Script                | Description                                      |
|-----------------------|--------------------------------------------------|
| `compression.py`      | Core SVD compression logic                       |
| `pull_push.py`        | Push compressed images to cloud + save metadata |
| `dag.py`              | Airflow DAG definition                           |
| `call_retrievers.py`  | API wrappers for image providers                 |
| `compress_upload.py`  | Entry point for batch compression and upload     |

---

## ✅ Skills 

- Distributed data engineering with **Airflow** and **PySpark**
- Image compression with **SVD** and NumPy
- Cloud-native architecture using **MongoDB** and **GCS**
- ML pipeline instrumentation with **MLflow**
- API-based ingestion, metadata management, and analytics-readiness

---

## 📜 License

MIT License

---

## ✍️ Author

Developed by Vitoria Lara
Built as a project to explore scalable image processing, cloud storage, and distributed computing.
