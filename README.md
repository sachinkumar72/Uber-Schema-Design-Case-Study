# Uber Schema Design Case Study

## 📌 Project Overview
This project is a **schema design case study of Uber**, one of the world’s leading ride-hailing platforms.  
The objective of this project is to analyze Uber’s core product features and design a structured **database schema** that represents how data could be stored, connected, and managed behind the platform.

This case study focuses on understanding how Uber’s backend system may handle users, drivers, rides, trip requests, locations, payments, ratings, and notifications through a relational data model.

The project demonstrates how **schema design supports real-world product functionality, scalability, and operational efficiency**.

---

## 🎯 Objective
The main objective of this project is to:

- Study Uber’s core platform functionality
- Identify major product entities and user interactions
- Design a structured schema for ride-booking operations
- Define relationships between users, drivers, rides, payments, and ratings
- Understand how backend data architecture supports real-world digital platforms

---

## 🛠 Skills Applied
This project demonstrates the following skills:

- Product analysis
- Schema design
- Database modeling
- Entity Relationship (ER) design
- Relational database understanding
- Backend system thinking
- Data architecture planning

---

## 🚖 About Uber as a Platform
Uber is a ride-booking platform that connects **riders** with **drivers** through a mobile application.  
The platform allows users to:
- Create an account
- Book rides
- Choose pickup and drop locations
- View fare estimates
- Make payments
- Rate drivers and rides
- Receive notifications and trip updates

Because Uber handles millions of ride requests, its backend data architecture must be **organized, scalable, and efficient**.

---

## 🏗 Project Approach
The project was completed in the following stages:

### 1. Feature Analysis
Uber’s major features were analyzed, such as:
- User registration and authentication
- Driver onboarding
- Ride booking
- Ride assignment
- Pickup and drop tracking
- Payment processing
- Ratings and reviews
- Notifications and ride history

### 2. Entity Identification
The platform was broken down into major entities based on functionality.

### 3. Attribute Mapping
Important fields were identified for each entity.

### 4. Relationship Design
Entity relationships were designed to represent how data flows through the platform.

### 5. Schema Structuring
A database schema was created to logically organize Uber’s operational data.

---

## 🧱 Core Entities in Uber Schema Design
The schema design includes the following major entities:

- **Users**
- **Drivers**
- **Vehicles**
- **Rides**
- **Ride Requests**
- **Locations**
- **Payments**
- **Ratings**
- **Promotions / Coupons**
- **Notifications**
- **Trip History**

---

## 🗂 Key Entities and Description

### 1. Users
Stores information about riders using the platform.

**Example attributes:**
- user_id
- full_name
- email
- phone_number
- password_hash
- profile_photo
- created_at
- account_status

---

### 2. Drivers
Stores information about drivers registered on the platform.

**Example attributes:**
- driver_id
- full_name
- phone_number
- email
- license_number
- rating
- availability_status
- created_at

---

### 3. Vehicles
Stores vehicle details linked to drivers.

**Example attributes:**
- vehicle_id
- driver_id
- vehicle_model
- vehicle_number
- vehicle_type
- color
- seating_capacity

---

### 4. Ride Requests
Stores booking requests created by users.

**Example attributes:**
- request_id
- user_id
- pickup_location_id
- drop_location_id
- requested_time
- ride_type
- estimated_fare
- request_status

---

### 5. Rides
Stores actual completed or ongoing ride details.

**Example attributes:**
- ride_id
- request_id
- driver_id
- vehicle_id
- ride_start_time
- ride_end_time
- distance_km
- final_fare
- ride_status

---

### 6. Locations
Stores pickup and drop location details.

**Example attributes:**
- location_id
- latitude
- longitude
- address
- city
- state
- country
- postal_code

---

### 7. Payments
Stores payment transactions for rides.

**Example attributes:**
- payment_id
- ride_id
- user_id
- payment_method
- payment_status
- amount_paid
- transaction_time

---

### 8. Ratings
Stores feedback and ratings given after rides.

**Example attributes:**
- rating_id
- ride_id
- user_id
- driver_id
- rating_score
- review_text
- created_at

---

### 9. Notifications
Stores user and driver notifications.

**Example attributes:**
- notification_id
- user_id
- driver_id
- notification_type
- message
- is_read
- created_at

---

### 10. Promotions / Coupons
Stores discount and promotional offers.

**Example attributes:**
- promo_id
- promo_code
- discount_type
- discount_value
- valid_from
- valid_to
- usage_limit

---

## 🔗 Entity Relationships
The relationships between the entities are designed as follows:

- One **User** can create many **Ride Requests**
- One **Driver** can complete many **Rides**
- One **Driver** can have one or more **Vehicles**
- One **Ride Request** can become one **Ride**
- One **Ride** is linked to one **Payment**
- One **Ride** can have one or more **Ratings**
- One **Ride Request** includes one **Pickup Location** and one **Drop Location**
- One **User** can receive many **Notifications**
- One **Driver** can receive many **Notifications**

These relationships help in maintaining data consistency and operational flow.

---

## 🧮 Example Schema Logic
Some example relational logic in this design:

- `user_id` in **Ride Requests** connects to **Users**
- `driver_id` in **Rides** connects to **Drivers**
- `vehicle_id` in **Rides** connects to **Vehicles**
- `ride_id` in **Payments** connects to **Rides**
- `ride_id` in **Ratings** connects to **Rides**
- `location_id` connects pickup and drop addresses

This makes the schema efficient for storing and retrieving ride-related data.

---

## 📊 Learning Outcome
Through this project, I gained a deeper understanding of:

- How ride-booking platforms are structured
- How real-world products are broken into entities and relationships
- How schema design supports platform scalability
- How backend data modeling impacts product functionality

This case study strengthened my understanding of **database architecture and product system thinking**.

---

## 🚀 Project Deliverables
This repository may include:

- Case Study Report
- Uber Schema Design Notes
- Entity Relationship Diagram (ERD)
- Database Table Structure
- README Documentation

---

## 📌 Use Case of This Project
This project is useful for:

- Product design learning
- Database design practice
- Backend architecture understanding
- System design portfolio building
- Academic case study submissions

---

## 👨‍💻 Author
**Sachin Kumar**

This project was created as part of a **schema design / product case study assignment** to understand how Uber’s backend data structure can be modeled through relational database design.
