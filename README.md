# 🏏 IPL Analytics Dashboard

An interactive **IPL Data Analytics Dashboard** built using **Django (Backend)** and **ReactJS (Frontend)**.  
It visualizes IPL statistics such as matches per year, team wins, and top economical bowlers using dynamic and responsive charts.

---

## 📊 Project Overview

- **IPL Analytics Dashboard** is a full-stack web application built with **Django REST Framework** and **ReactJS**, designed to visualize and analyze **Indian Premier League (IPL)** data.

- It processes large CSV datasets (`matches.csv`, `deliveries.csv`) and provides rich analytical insights through RESTful APIs.  
The frontend consumes these APIs to display visually appealing charts using **Chart.js** and **Material-UI** components.

- **Backend:**  Django + Django REST Framework (API endpoints that aggregate IPL data)
- **Frontend:**  React (Material-UI) + react-google-charts for interactive charts

- It uses the Kaggle IPL dataset (matches.csv, deliveries.csv) and exposes endpoints to power the UI for the following tasks:
1. Matches played per year (landing page — chart #1)
2. Stacked bar chart of matches won by teams across seasons (landing page — chart #2)
3. For a given year YYYY: extra runs conceded per team
4. For a given year YYYY: top economical bowlers
5. For a given year YYYY: matches played vs matches won per team

## 🧠 Key Features

- 📅 Matches played per year (Bar Chart)
- 🏆 Matches won by each team (Stacked Bar Chart)
- 🎯 Extra runs conceded per team (Year-wise)
- 💰 Top economical bowlers (Year-wise)
- ⚔️ Matches played vs matches won for each team

---

## 🧩 Tech Stack

**Frontend:** ReactJS, Axios, Chart.js, Material-UI  
**Backend:** Django, Django REST Framework  
**Database:** SQLite (default, can be replaced with PostgreSQL/MySQL)  
**Languages:** Python 3.x, JavaScript (ES6)  

---
## 🖥️ Dashboard Preview
Chart	Description
- 📅 Matches per Year	Bar chart of total matches played each season
- 🏆 Matches Won	Stacked bar chart of total wins by each team
- 🎯 Extra Runs	Year-wise extra runs conceded by each team
- 💰 Economical Bowlers	Top economical bowlers for a selected season
- ⚔️ Matches Played vs Won	Performance comparison for each team

## ⚙️ Setup Instructions

### 🔹 Backend Setup (Django)

```bash
# Clone Repository
git clone https://github.com/<your-username>/IPL-Analytics-Dashboard.git
cd backend

# Create Virtual Environment
python -m venv venv

# Activate Virtual Environment
# (Windows)
venv\Scripts\activate
# (Linux/Mac)
source venv/bin/activate

# Install Dependencies
pip install -r requirements.txt

# Run Migrations
python manage.py migrate

# Load IPL Dataset (optional script)
python manage.py loaddata ipl_data.json  # or custom CSV load script

# Start Backend Server
python manage.py runserver
```
API Base URL:
- 👉 http://127.0.0.1:8000/api/

### 🔹 Frontend Setup (ReactJS)
```bash
Open a new terminal and run:
cd frontend
npm install
npm start
```
Frontend URL:
- 👉 http://localhost:3000/

## 🧮 Dataset
- Download the IPL dataset from Kaggle:
- 📂 IPL Dataset – Kaggle - https://www.kaggle.com/datasets/manasgarg/ipl
