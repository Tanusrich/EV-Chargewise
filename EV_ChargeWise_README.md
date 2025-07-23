
# ⚡ EV ChargeWise

EV ChargeWise is a full-stack mobile application designed to simplify the process of finding, booking, and paying for Electric Vehicle (EV) charging stations. With real-time availability, smart booking, route optimization, and secure payments, the app provides a seamless and efficient charging experience for EV users.

---

## 🚀 Features

### 👥 User Features
- 🔍 **Find Charging Stations** using real-time availability and geolocation.
- 🗺️ **Route Optimization** with OSRM API integration to suggest best routes with charging stops.
- 🕑 **Smart Slot Booking** in real-time with time-based availability.
- 💳 **Secure Payments** via PayPal integration using in-app WebView.
- 📱 **Cross-Platform App** built with Flutter for both Android and iOS.

### 🛠️ Admin Features
- ⚙️ Manage stations (add, update, toggle maintenance mode).
- 📊 Monitor bookings, station performance, and availability.
- 🔐 Role-based access (Admin and Super Admin).
- 🧠 Background task handling for booking expiration and payment verification.

---

## 🧠 Tech Stack

### 🔧 Backend
- **FastAPI** (Python) – RESTful APIs
- **PostgreSQL** – Relational database
- **SQLAlchemy + Alembic** – ORM and migrations
- **Redis + Celery** – Async task queue
- **PayPal SDK** – Payment integration
- **OSRM + Dijkstra Algorithm** – Route optimization
- **JWT Authentication** – Secure login system

### 📱 Frontend
- **Flutter (Dart)** – Cross-platform app
- **Provider** – State management
- **flutter_map + latlong2** – Map integration using OpenStreetMap
- **http, shared_preferences, flutter_webview** – Core services & in-app PayPal flow

---

## 📊 Architecture

```mermaid
flowchart TD
    UserApp[User App (Flutter)]
    AdminApp[Admin App (Flutter)]
    Frontend -->|REST API| Backend
    Backend -->|PostgreSQL| Database[(PostgreSQL)]
    Backend -->|Redis| TaskQueue[(Celery)]
    Backend --> PayPal[PayPal API]
    Backend --> OSRM[OSRM Server]
    Frontend --> Leaflet[Map API (flutter_map)]
    Backend --> Auth[JWT Auth]

    subgraph Frontend
        UserApp
        AdminApp
    end
```

---

## 📚 Data Collection & Research

We scraped real-world EV charging station data for analysis and training:
- 🔗 **https://www.statiq.in/ev-charging-station**
- 🔗 ElectricPe (Hyderabad)
- 🔗 e-AMRIT (Government Portal)

We analyzed:
- ⚡ Charging types and parameters
- 💰 Pricing models
- 🧮 Cost and energy consumption calculations using Public Charging Calculator

---

## 🏗️ Core Modules

- **Station Management**
- **Slot Booking System**
- **Payment Handling**
- **Role-Based Access Control**
- **Route Optimization**
- **Dashboard Metrics**

---

## 📦 Installation & Run (Local)

### Backend
```bash
cd backend
python -m venv env
source env/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend (Flutter)
```bash
cd frontend
flutter pub get
flutter run
```

---

## 📌 Future Scope

- 🔁 Deploy on Play Store / Web
- 🛜 Real-time charger status via IoT integration
- 📈 Dynamic pricing based on usage/demand
- 🅿️ Slot pre-booking with cancelation policy

---

## 🤝 Contributors

- **Tanusri Ch** – Full Stack Developer (Frontend & Backend)
- Team Members: [Add more if applicable]

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).
