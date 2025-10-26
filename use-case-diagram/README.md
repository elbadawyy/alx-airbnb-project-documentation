# 🎭 Airbnb Clone – Use Case Diagram

This document presents the **Use Case Diagram** for the **Airbnb Clone backend system**, visualizing how different actors interact with the system to accomplish various functionalities.

---

## 🎯 Objective
The goal of this diagram is to illustrate:
- The **main actors** in the Airbnb Clone system (e.g., Guest, Host, Admin, Payment Gateway).
- The **use cases** (actions) they can perform.
- The **relationships** between actors and system features.

---

## 🧍 Actors
| Actor | Description |
|-------|--------------|
| **Guest (User)** | A user who browses listings, makes bookings, and leaves reviews. |
| **Host** | A user who lists properties, manages availability, and accepts bookings. |
| **Admin** | Oversees the platform, manages users, and moderates listings/reviews. |
| **Payment Gateway** | External service for handling payments and refunds securely. |

---

## ⚙️ Key Use Cases
### For **Guest**
- Register / Login  
- Browse and search properties  
- View property details  
- Book a property  
- Make a payment  
- Cancel booking  
- Leave a review  
- Send messages to host

### For **Host**
- Register / Login  
- Create and manage listings  
- Update property availability  
- View and manage bookings  
- Respond to messages  
- View guest reviews

### For **Admin**
- Manage users (Guests, Hosts)  
- Approve or remove listings  
- View reports and analytics  
- Handle refund or dispute cases

### For **Payment Gateway**
- Process booking payments  
- Handle refunds for cancellations