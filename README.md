# 🎧 AWS Data Engineering Pipeline: Music Data Analysis

This project demonstrates an end-to-end data engineering workflow using **AWS Glue**, **Pandas**, and **Amazon QuickSight** to transform, analyze, and visualize music streaming metadata (tracks, albums, artists).

---

## 📌 Overview

We built a cloud-based pipeline that:
- Cleans and transforms raw data using **AWS Glue Studio (Visual Jobs)**
- Performs analytical queries using **Pandas**
- Visualizes insights with **Amazon QuickSight**

---

## 🗂️ Dataset

The project uses 3 core datasets:
- `tracks.csv` — Track metadata (duration, popularity, genre)
- `albums.csv` — Album information (release, artist ID, etc.)
- `artists.csv` — Artist profile and popularity

All files are stored in **Amazon S3** and processed with Glue.

---

## 🛠️ Technologies Used

| Service/Library | Purpose |
|-----------------|---------|
| **AWS Glue Studio (Visual)** | ETL: joins, filters, field renames, calculated fields |
| **Amazon S3** | Data storage (raw + cleaned) |
| **Pandas (Python)** | Data analysis & grouping |
| **Amazon QuickSight** | Dashboards and insights |
| **IAM Roles + CloudWatch** | Logging and permissions |

---

## 🔄 Pipeline Architecture

```text
S3 (raw CSVs)
   ↓
AWS Glue (Visual Jobs: Join, Clean, Transform)
   ↓
S3 (cleaned Parquet or CSV)
   ↓
Pandas (via Jupyter Notebook)
   ↓
QuickSight (visualize metrics)
