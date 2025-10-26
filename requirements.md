# 🏗️ Backend Requirement Specifications — Airbnb Clone

This document outlines the **technical and functional requirements** for three key backend features of the Airbnb Clone project:

1. User Authentication  
2. Property Management  
3. Booking System  

Each feature includes API endpoint details, input/output specifications, validation rules, and performance expectations.

---

## 1. 🔐 User Authentication

### **Overview**
The authentication system enables users to register, log in, and manage sessions securely.  
It ensures data privacy and protects against unauthorized access using JWT (JSON Web Token) authentication.

### **Functional Requirements**
- Users must be able to create an account with unique email addresses.
- Passwords must be securely hashed before storage.
- Users must be able to log in and receive a valid JWT token.
- Tokens should expire after a defined duration (e.g., 24 hours).
- The system must validate tokens for every protected endpoint.

### **API Endpoints**

| Method | Endpoint              | Description                   | Authentication |
|:-------:|:----------------------|:-------------------------------|:---------------|
| POST    | `/api/register`       | Register a new user            | ❌ No          |
| POST    | `/api/login`          | Log in existing user           | ❌ No          |
| GET     | `/api/profile`        | Retrieve authenticated user    | ✅ Yes         |
| POST    | `/api/logout`         | Invalidate user session/token  | ✅ Yes         |

### **Input Validation Rules**
| Field | Type | Constraints |
|:------|:-----|:------------|
| `name` | string | Required, min: 3 chars |
| `email` | string | Required, must be unique and valid format |
| `password` | string | Required, min: 8 chars, must include letters and numbers |

### **Response Examples**
**Success (Login):**
```json
{
  "message": "Login successful",
  "token": "eyJhbGciOiJIUzI1NiIsInR5..."
}
