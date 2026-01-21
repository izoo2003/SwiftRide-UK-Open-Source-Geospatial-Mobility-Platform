# 🚗 SwiftRide UK: Open-Source Geospatial Mobility Platform

SwiftRide UK is a full-stack, open-source ride-hailing solution specifically engineered for the United Kingdom market. The platform leverages high-performance backend architecture and cost-effective geospatial logic to provide a seamless booking experience, real-time fare estimation, and interactive route tracking.

---

## ✨ Key Features

- **Dynamic Booking Engine**: Users can create accounts, select from various car types (Economy, Luxury, Van), and book rides across the UK.
- **Geospatial Intelligence**: Integrated **OSRM (Open Source Routing Machine)** and **OpenStreetMap** for real-time distance calculations and optimized route plotting without expensive API overhead.
- **Smart Fare Estimation**: Automated calculation of travel costs based on distance, time, and vehicle category.
- **Real-Time Tracking**: Persistent record management allowing users to track their booking history and current ride status.
- **High-Concurrency Architecture**: Built with a focus on speed and reliability using a FastAPI backend.

---

## ⚡ Tech Stack

- **Frontend**: [React.js](https://react.dev/) — Interactive, responsive UI with real-time state management.
- **Backend API**: [FastAPI](https://fastapi.tiangolo.com/) — High-performance Python framework for handling geospatial logic and booking concurrency.
- **Database**: [Supabase (PostgreSQL)](https://supabase.com/) — Secure user authentication and robust relational data management for booking records.
- **Mapping & Routing**: [OSRM](http://project-osrm.org/) + [OpenStreetMap](https://www.openstreetmap.org/) — Self-hosted, open-source geospatial engine for routing and distance services.
- **Styling**: Tailwind CSS — Modern, sleek utility-first styling.

---

## 📂 Project Structure

| Directory | Purpose |
| :--- | :--- |
| `/frontend` | React.js source code, including booking forms, interactive maps, and user dashboards. |
| `/backend` | FastAPI application containing geospatial service wrappers and API endpoints. |
| `/database` | Supabase schema definitions and PostgreSQL migration scripts for booking logs. |
| `/services` | Integration logic for OSRM route processing and fare calculation algorithms. |

---

## 🛠️ Project Setup

### 1. Prerequisites
Ensure you have the following installed:
- Node.js & npm/yarn
- Python 3.9+
- A Supabase project instance

### 2. Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
