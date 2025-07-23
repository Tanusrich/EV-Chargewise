
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

<img width="851" height="420" alt="image" src="https://github.com/user-attachments/assets/69c07955-f835-4c32-b140-cd173d9f1d02" />

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

## 📦 App UI

### User
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/3f5b732c-25a3-4ce0-a72e-e5573e608dc1" /> 
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/ecb7628a-8c1d-44ef-bff3-e0203d713bc8" /> 
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/279435a8-212a-4b46-a7b3-9d3a7fd1137c" />
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/a0414dba-a626-4be2-b434-9170d42ee5fd" />
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/1bb2f9d1-41b9-4b8e-bfa6-da6c68197c74" /> <img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/6740a05b-b29e-4f3c-b655-ad5c089d688d" />

### Admin
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/b88049fe-d6a4-4124-960e-afee6de2ce97" /> <img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/12e7e2b7-16aa-4320-b689-e16cf5326ae3" />
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/543550c6-ce7f-46c1-b183-bcadf48ef6b1" />

### Super Admin
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/7492f66e-1985-4931-9b00-4773202f0541" />
<img width="207" height="461" alt="image" src="https://github.com/user-attachments/assets/49accc0e-07e2-4720-9bab-26d2de480bbe" />

---

## 🤝 Contributors

- **Tanusri Ch**
- **Vedika Heda**
- **Thrishala Ch**
- **Aadhya Reddy**

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).
