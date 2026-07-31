# 🏭 AI Enterprise Synthetic Data Factory

> **Generate high-quality synthetic enterprise datasets for ML training while preserving privacy and statistical characteristics**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [System Architecture](#-system-architecture)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [Usage Guide](#-usage-guide)
- [API Endpoints](#-api-endpoints)
- [Privacy & Security](#-privacy--security)
- [Evaluation Metrics](#-evaluation-metrics)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

The **AI Enterprise Synthetic Data Factory** is a comprehensive platform that solves the critical data bottleneck faced by enterprise AI initiatives. By generating privacy-preserving synthetic data, it enables organizations to:

- **Accelerate AI Development** - Reduce data preparation time from days to minutes
- **Ensure Privacy Compliance** - Generate GDPR/CCPA compliant datasets
- **Enable Data Sharing** - Safely share data across teams and partners
- **Augment Sparse Data** - Create edge cases and rare scenarios for robust model training

> ⚠️ **Note**: This is a **practice/learning project** designed for CPU-only environments. Not intended for production deployment.

---

## ✨ Key Features

### 🤖 Multi-Model Data Generation
| Model | Use Case | Best For |
|-------|----------|----------|
| **CTGAN** | Tabular data synthesis | Mixed-type enterprise data |
| **Diffusion Models** | High-fidelity generation | Complex structured datasets |
| **TVAE** | Variational autoencoder | Large-scale data generation |
| **Gemini API** | Intelligent data augmentation | Natural language data requests |

### 🔒 Privacy Preservation
- **Differential Privacy** with adjustable epsilon/delta budgets
- **Privacy-Utility Tradeoff** visualization
- **Membership Inference Protection** against attacks
- **GDPR Compliance** ready synthetic data

### 📊 Quality Validation
- **Kolmogorov-Smirnov Test** for distribution similarity
- **Total Variation Distance (TVD)** for statistical fidelity
- **Machine Learning Usability (TSTR)** - Train on Synthetic, Test on Real
- **LLM-as-Judge** validation workflow

### 🎨 User Experience
- **Interactive Dashboard** with real-time visualizations
- **One-Click Export** to CSV, JSON, or Parquet
- **Natural Language Queries** via Gemini integration
- **Responsive Design** optimized for all devices

---

## 🛠️ Technology Stack

### Backend
```yaml
Framework: FastAPI 0.100+
Languages: Python 3.9+
ML Libraries: 
  - CTGAN (SDV Library)
  - PyTorch (CPU optimized)
  - diffprivlib (Differential Privacy)
Database: SQLite (lightweight)
API Integration: Google Gemini API
Data Processing: pandas, numpy, scikit-learn

Framework: React 18+
Styling: Tailwind CSS + Material-UI
Charts: Chart.js / D3.js
State Management: React Context API
HTTP Client: Axios
Build Tool: Vite / Create React App

# 1. Navigate to backend
cd backend

# 2. Create virtual environment
python -m venv venv

# 3. Activate virtual environment
# Windows
venv\Scripts\activate
# Mac/Linux
source venv/bin/activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Create .env file
cp .env.example .env

# 6. Edit .env with your Gemini API key
# GEMINI_API_KEY=your_api_key_here

# 7. Initialize database
python scripts/setup_db.py

# 8. Run the server
uvicorn app.main:app --reload

# 1. Navigate to frontend
cd frontend

# 2. Install dependencies
npm install

# 3. Create .env file
cp .env.example .env

# 4. Start the development server
npm start