# AppointmentScheduler-SpringBoot

# 🩺 Schedula - Debugging Dynamos Backend (Spring Boot Edition)

A scalable, modular **backend API** for a **Hospital Appointment Scheduling System**, rebuilt using **Spring Boot**, **Java 17**, and **PostgreSQL**.

This backend system provides a robust platform for managing appointments, doctors, patients, and administrative functions in a clinical environment.

---

### 🚀 Key Features

- ### 🧠 **Elastic Scheduling**
  Doctors can dynamically shrink or expand available sessions in real-time, adjusting to demand or changes.

- ### 🌊 **Wave Scheduling**
  Supports advanced scheduling logic (e.g., **wave scheduling**) to reduce patient wait times and increase operational efficiency.

- ### 🔐 **Role-Based Access Control**
  Secure, token-based access control for doctors, patients, and admins.

- ### 👥 **Robust User Management**
  Comprehensive APIs for managing doctor/patient profiles, appointment bookings, and notifications with validations.

- ### 🧱 **Scalable Architecture**
  A modular Spring Boot architecture based on layered design principles: **Controller → Service → Repository (JPA)**.

---

## 📦 Tech Stack

| Tech                | Version      |
|---------------------|--------------|
| Java                | 17+          |
| Spring Boot         | 3.x          |
| Spring Security     | ✅           |
| PostgreSQL          | 15+          |
| Spring Data JPA     | ✅           |
| JWT Authentication  | ✅           |
| Swagger / OpenAPI   | ✅           |
| Maven               | ✅           |
| Lombok              | ✅           |
| Email / JavaMail    | ✅           |
| Docker (optional)   | ✅           |

---

## 🛠️ Getting Started

### 🧾 Prerequisites

- Java 17+
- Maven
- PostgreSQL
- Git

---

### 📁 Clone the Repository

```bash
git clone https://github.com/Sayon008/AppointmentScheduler-SpringBoot.git
cd AppointmentScheduler-SpringBoot

# Database Config
spring.datasource.url=jdbc:postgresql://localhost:5432/schedula_db
spring.datasource.username=your_db_username
spring.datasource.password=your_db_password
spring.jpa.hibernate.ddl-auto=update

# JWT Config
jwt.secret=your_jwt_secret
jwt.expiration=3600000

# Email Config
spring.mail.username=your_email@example.com
spring.mail.password=your_email_password
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.protocol=smtp
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

```

### Create Database

```bash
CREATE DATABASE schedula_db;
```

### Project Structure

```angular2html
com.hospital.appointmentschedulingsystem
│
├── config/                        → security, CORS, JWT, etc.
│
├── controller/
│   ├── auth/
│   │   └── AuthController.java
│   ├── doctor/
│   ├── patient/
│   ├── appointment/
│
├── dto/
│   ├── auth/
│   │   ├── LoginRequest.java
│   │   ├── SignupRequest.java
│   │   └── AuthResponse.java
│   ├── doctor/
│   ├── patient/
│   ├── appointment/
│
├── entity/
│   ├── User.java
│   ├── Doctor.java
│   ├── Patient.java
│   ├── Appointment.java
│
├── repository/
│   ├── UserRepository.java
│   ├── DoctorRepository.java
│   ├── PatientRepository.java
│
├── service/
│   ├── auth/
│   │   ├── AuthService.java
│   │   └── impl/AuthServiceImpl.java
│   ├── doctor/
│   ├── patient/
│   ├── appointment/
│
├── security/
│   ├── JwtService.java
│   ├── JwtAuthFilter.java
│   └── SecurityConfig.java
│
├── exception/
│   ├── GlobalExceptionHandler.java
│   ├── CustomExceptions.java
│
└── AppointmentSchedulingSystemApplication.java

```