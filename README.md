# 🏏 IPL Analytics Dashboard

**IPL Analytics Dashboard** is a **full-stack web application** built with **Django REST Framework  (Backend)** and **ReactJS (Frontend)**, designed to visualize and analyze **Indian Premier League (IPL)** data.
It visualizes IPL statistics such as matches per year, team wins, and top economical bowlers using dynamic and responsive charts.

- It processes large CSV datasets (`matches.csv`, `deliveries.csv`) and provides rich analytical insights through RESTful APIs.  
- The frontend consumes these APIs to display visually appealing charts using **Chart.js** and **Material-UI** components.

## 📊 Project Overview
- **In the backend,** built with Django REST Framework, processes IPL data from CSV files and provides REST APIs for analytics like matches per year, team wins, and top bowlers.
- **In the frontend React,** I used `Axios` to call APIs from Django, `Chart.js` to visualize the IPL data in interactive graphs, and `Material-UI` to design a professional and responsive UI with ready-made React components (AppBar, Toolbar, Button).

## Key
- **Backend:**  Django + Django REST Framework (API endpoints that aggregate IPL data)
- **Frontend:**  React (Material-UI) + react-google-charts for interactive charts
  
### 1. Axios (API Calls)
- - `JavaScript library` used to make HTTP requests from the frontend to the backend (APIs)
- - Axios acts as the bridge between my React frontend and Django backend.
- - When a user visits a chart page, Axios requests data from my Django API — for example, `/api/matches-per-year/` — and then updates the chart dynamically.
### 2. Chart.js (Visualization)
- - Chart.js is a `charting library` that allows you to create beautiful, interactive graphs such as bar charts, line charts, pie charts, and more.
- - Chart.js handles the visualization part. Once Axios fetches the data from Django, I pass it to Chart.js to render a bar or stacked chart — for example, the total matches per year
### 3. Material-UI (UI Design)
- - Material-UI (now called MUI) is a `React component library` that implements Google’s Material Design — a modern design system for building clean, professional UIs.
- - Material-UI gave me ready-made components like AppBar, Button, and Card for quick and attractive UI development.
 
  
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
