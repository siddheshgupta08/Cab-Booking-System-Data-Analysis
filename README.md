# 🚖 Cab Booking System Data Analysis - MySQL Project

This article provides a step-by-step guide to understanding how a cab booking system efficiently stores, manages, and analyzes operational data.  
The project serves as a practical approach to learning fundamental database and backend concepts, including:

- Creating structured relational databases for cab operations  
- Inserting and managing customer, driver, cab, booking, and trip data  
- Running data analysis queries to reveal business insights  
- Measuring customer behavior, driver performance, and revenue trends  

By the end of this project, readers will understand how SQL is used to manage and analyze cab booking systems effectively.

---

# 📌 Project Overview

This case study simulates a cab booking company’s database system. The goal is to understand how structured data can be used to store, manage, and analyze real-world cab booking operations.  
You’ll create database tables, insert meaningful records, and write SQL queries to generate insights related to:

- Customer behavior  
- Driver performance  
- Trip efficiency  
- Revenue patterns  

---

# 🎯 Project Objectives

The main goals of this project are:

- Analyze cab booking patterns, customer behavior, and driver performance  
- Identify trends such as peak booking days, cancellation rates, and revenue patterns  
- Evaluate driver performance using ratings, earnings, and trip distances  
- Measure operational efficiency: wait times, trip types, route popularity  
- Generate insights to improve customer satisfaction and optimize cab allocation  
- Build SQL-based analytical queries for real-time business decision-making  

---

# 🗂️ Dataset Schema Overview

## 1️⃣ Customers Table

| Column              | Type       | Description                    |
|---------------------|------------|--------------------------------|
| **CustomerID**      | INT (PK)   | Unique customer ID             |
| **Name**            | VARCHAR    | Customer name                  |
| **Email**           | VARCHAR    | Email address                  |
| **RegistrationDate**| DATE       | Date when customer registered  |


## 2️⃣ Drivers Table

| Column        | Type       | Description              |
|---------------|------------|--------------------------|
| **DriverID**  | INT (PK)   | Unique driver ID         |
| **Name**      | VARCHAR    | Driver name              |
| **JoinDate**  | DATE       | Driver joining date      |


## 3️⃣ Cabs Table

| Column          | Type       | Description                       |
|-----------------|------------|-----------------------------------|
| **CabID**       | INT (PK)   | Cab ID                            |
| **DriverID**    | INT (FK)   | Assigned driver                   |
| **VehicleType** | VARCHAR    | Sedan, SUV, etc.                  |
| **PlateNumber** | VARCHAR    | Vehicle registration number       |


## 4️⃣ Bookings Table

| Column              | Type       | Description                  |
|---------------------|------------|------------------------------|
| **BookingID**       | INT (PK)   | Booking ID                   |
| **CustomerID**      | INT (FK)   | Customer who booked          |
| **CabID**           | INT (FK)   | Cab involved                 |
| **BookingDate**     | DATETIME   | Booking timestamp            |
| **Status**          | VARCHAR    | Completed / Canceled         |
| **PickupLocation**  | VARCHAR    | Start location               |
| **DropoffLocation** | VARCHAR    | End location                 |


## 5️⃣ TripDetails Table

| Column         | Type       | Description                 |
|----------------|------------|-----------------------------|
| **TripID**     | INT (PK)   | Trip ID                     |
| **BookingID**  | INT (FK)   | Linked booking              |
| **StartTime**  | DATETIME   | Trip start time             |
| **EndTime**    | DATETIME   | Trip end time               |
| **DistanceKM** | FLOAT      | Total kilometers traveled   |
| **Fare**       | FLOAT      | Fare charged                |


## 6️⃣ Feedback Table

| Column         | Type     | Description                     |
|----------------|----------|---------------------------------|
| **FeedbackID** | INT (PK) | Feedback ID                     |
| **BookingID**  | INT (FK) | Related booking                 |
| **Rating**     | FLOAT    | Rating (1–5)                    |
| **Comments**   | TEXT     | Customer feedback               |
| **FeedbackDate**| DATE    | Date feedback was submitted     |

---

# 🛠️ Tools & Technologies Used

### **Database**
- MySQL  

### **Tools**
- MySQL Workbench  

---

# 🖼️ ER Diagram

<img width="751" height="651" alt="image" src="https://github.com/user-attachments/assets/d8403d45-b571-4c8e-94a7-008945176de2" />

---

# 📊 Key Insights You Can Derive

### 🔹 Customer Insights  
- Which customers complete the most rides  
- Customers with cancellation rates over 30%  
- Customer loyalty & usage patterns  

### 🔹 Driver Insights  
- Drivers with low ratings in the last 3 months  
- Drivers generating the highest revenue  
- Drivers with cancellation rates above 25%  
- Best-performing drivers by distance  

### 🔹 Trip & Booking Insights  
- Busiest day of the week  
- Most popular routes (Pickup → Dropoff)  
- Revenue comparison: short vs long trips  
- Weekend vs weekday performance  
- Average wait time per pickup location  

### 🔹 Revenue Insights  
- Monthly revenue trends (last 6 months)  
- Revenue by vehicle type (Sedan vs SUV)  
- Drivers ranked by earnings  

---

# 🌟 Project Impact

This project helps a cab company:

✔ Optimize driver & cab allocation  
✔ Improve customer satisfaction  
✔ Reduce cancellations with data-backed insights  
✔ Boost revenue using trend-based strategies  
✔ Enable real-time, data-driven decisions  

---

# ❓ List of SQL Queries Used in Analysis

1. Completed bookings per customer  
2. Customers with >30% cancellation rate  
3. Busiest day of the week  
4. Drivers with rating <3 in the last 3 months  
5. Top 5 drivers by total distance traveled  
6. Drivers with >25% cancellation rate  
7. Monthly revenue (last 6 months)  
8. Top 3 busiest routes  
9. Driver ratings vs earnings analysis  
10. Average wait time by pickup location  
11. Short vs long trip revenue  
12. Revenue by vehicle type  
13. Weekend vs weekday comparison  

---

# 🏁 Conclusion

This project demonstrated the power of SQL in transforming cab booking operations
data into actionable business insights. From customer behavior and driver performance
to revenue trends and operational efficiency, each query revealed patterns that help
optimize services, improve user satisfaction, and guide data-driven decision-making.
Well-structured SQL logic can empower strategic planning and improve real-world
business outcomes.

