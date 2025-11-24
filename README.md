# HackTheTrack
Hack the Track presented by Toyota GR
# GR Cup Strategy Center

Video Description: https://www.loom.com/share/d87e97dc44d24d878b3e832f15dce14d

## Overview
The **GR Cup Strategy Center** is a cutting-edge, real-time race strategy and psychology analysis platform designed for the Toyota GR Cup. It combines telemetry data, Monte Carlo simulations, and AI-driven psychological profiling to provide race engineers and drivers with actionable insights.

This platform is built to give teams a competitive edge by decoding not just the car's performance, but also the driver's mental state and the strategic landscape of the race.

## Key Features

### 1. Dashboard
The central hub for real-time race monitoring. It provides a high-level overview of the current race status, including track conditions, leaderboards, and critical alerts.

### 2. Performance (Telemetry)
A dedicated section for visualizing live telemetry streams.
- **Real-time Charts:** Monitor speed, throttle, brake, and steering inputs.
- **Data Analysis:** Identify performance gaps and optimize driving lines.

### 3. Simulation Engine (Strategy)
A powerful Monte Carlo simulation engine for race strategy planning.
- **Probabilistic Modeling:** Run thousands of race simulations to predict outcomes based on tire degradation, fuel load, and pace variability.
- **Inline Reporting:** View detailed simulation reports directly on the dashboard.
- **PDF Export:** Download comprehensive strategy reports for offline analysis.

### 4. Predictions
AI-driven predictive models for race pace and tire life.
- **Pace Prediction:** Forecast lap times based on fuel load and tire wear.
- **Tire Degradation:** Estimate remaining tire life to optimize pit stop windows.

### 5. Analysis
Post-race analysis tools to review performance and strategy execution.
- **Historical Data:** Compare current performance against historical benchmarks.
- **Session Review:** Deep dive into specific race sessions.

### 6. Psychology (Mental Game Decoder)
An industry-first AI module for analyzing driver psychology.
- **Track Profiling:** Analyzes tracks (e.g., Barber, COTA, Indy) to identify high-stress zones and confidence traps.
- **Mental State Analysis:** Uses telemetry patterns to infer driver stress, focus, and confidence levels.
- **AI Coaching:** Provides real-time, context-aware coaching tips to help drivers maintain peak mental performance.
- **Enneagram Visualization:** Visualizes the track's psychological profile using a 5-point radar chart (Stress, Focus, Rhythm, Aggression, Technicality).

## Technology Stack

- **Frontend:** React, TypeScript, Material UI, Recharts, Framer Motion
- **Backend:** Python (FastAPI/Flask), NumPy, Scikit-learn
- **Data Streaming:** WebSocket (simulated real-time telemetry)
- **PDF Generation:** html2canvas, jsPDF

## Installation & Usage

### Prerequisites
- **Node.js** (v16 or higher)
- **Python** (v3.9 or higher)

### Docker Setup (Recommended)
The easiest way to run the application is using Docker Compose. This will set up the backend, frontend, database, and Redis cache automatically.

1.  Ensure you have Docker and Docker Compose installed.
2.  Run the following command from the root directory:
    ```bash
    docker-compose up -d --build
    ```
3.  Access the application:
    - Frontend: `http://localhost:3000`
    - Backend API: `http://localhost:8000`

For more detailed instructions, see [INSTALLATION.md](INSTALLATION.md).

### Manual Setup
If you prefer to run the application locally without Docker (or only use Docker for the database), follow these steps:

### Backend Setup
1.  Navigate to the backend directory:
    ```bash
    cd backend
    ```
2.  Create a virtual environment:
    ```bash
    python -m venv venv
    ```
3.  Activate the virtual environment:
    - Linux/Mac: `source venv/bin/activate`
    - Windows: `venv\Scripts\activate`
4.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
5.  Start the backend server:
    ```bash
    python main.py
    ```
    The backend will run on `http://localhost:8000`.

### Frontend Setup
1.  Navigate to the frontend directory:
    ```bash
    cd frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the development server:
    ```bash
    npm start
    ```
    The application will open in your browser at `http://localhost:3000`.

### Quick Start (Development)
For a streamlined development experience, you can start both the backend and frontend servers concurrently using the following command from the root directory:

1.  Ensure dependencies are installed for both backend and frontend (see above).
2.  Run the development script from within the gr-cup-strategy-center directory:
    ```bash
    npm run dev
    ```
    This will start the backend on port 8000 and the frontend on port 3000.

## License
Proprietary software developed for the Toyota GR Cup. All rights reserved.
