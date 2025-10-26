# 🔄 Airbnb Clone – Data Flow Diagram (DFD)

This document explains the **Data Flow Diagram (DFD)** for the **Airbnb Clone Backend System**, showing how data moves between users, the backend, and the database.

---

## 🧠 Objective

The goal of this diagram is to visualize:
- How **data is collected** (inputs) from users and system processes  
- How it is **processed** by backend logic (controllers, services, APIs)  
- How it is **stored and retrieved** from the database  
- How **responses** are returned to users or external systems

---

## 🗺️ Diagram Overview

The DFD represents the **flow of data** among the key entities and subsystems of the Airbnb backend, including:

1. **User (Guest / Host / Admin)**
2. **Property Service**
3. **Booking Service**
4. **Payment Service**
5. **Database**

Each data flow demonstrates the interaction between these entities and how user actions translate into backend processes and database transactions.

---

## 📊 DFD Structure (Level 1)

### **1. User Interactions**
- **Input:** User submits login, registration, booking, or property actions.
- **Process:** Requests are handled by the backend API (authentication, validation, and logic).
- **Output:** The system returns responses such as confirmations, booking details, or error messages.

### **2. Property Management**
- **Input:** Host submits property data (title, description, images, price, availability).
- **Process:** Property Service validates and stores details in the database.
- **Output:** Property listings are returned to users searching for stays.

### **3. Booking Process**
- **Input:** Guest initiates booking request.
- **Process:** System checks property availability and creates a booking record.
- **Output:** Confirmation is sent to the guest and host dashboards.

### **4. Payment Processing**
- **Input:** Guest confirms booking and provides payment info.
- **Process:** Payment Service securely processes payment via a third-party gateway (e.g., Stripe).
- **Output:** Payment confirmation stored; receipt generated for user.

### **5. Database Layer**
- Centralized storage for **users, properties, bookings, reviews, and transactions.**
- Supports CRUD operations and maintains data integrity.

---

## 🖼️ Diagram File

📁 **File Name:** `data-flow.png`  
🗂️ **Directory:** `data-flow-diagram/`  

The diagram visually represents how requests, processes, and responses connect across the system layers.

---

## 🧩 Example Data Flow Summary

| Process | Input | Data Transformation | Output |
|----------|--------|--------------------|---------|
| User Login | Credentials | Validate → Token Generation | Auth Token |
| Property Creation | Property Details | Validate → Store → Index | Property ID |
| Booking | Booking Request | Check Availability → Create Record | Booking Confirmation |
| Payment | Payment Info | Process via API → Update Status | Payment Receipt |

---