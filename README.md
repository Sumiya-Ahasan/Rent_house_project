# 🏡 Dream Nest

Dream Nest is an **all-in-one online platform** that simplifies buying, renting, and decorating homes.  
It caters to diverse roles such as renters, buyers, builders, home decorators, and administrators, focusing on **streamlining real estate transactions and property management** through a user-friendly interface.

---

## 🚀 Motivation
Real estate tasks—property management, sales, rentals, and renovations—are often **complex and time-consuming**.  
Dream Nest addresses these challenges by offering a **unified platform** where users can handle all their real estate needs with ease.

✅ Whether selling a home, exploring rental options, or managing relocation/renovation services, Dream Nest ensures **speed, convenience, and efficiency**.

---

## ✨ Features

1. **User Management**
   - Registration and login
   - Role-based access (user, builder, admin)

2. **Property Listings**
   - Add properties for sale or rent
   - Include price, type, status, images, and details

3. **Rental Reviews**
   - Submit and view reviews of rental services

4. **Service Management**
   - Track relocation, packing, and renovation services

5. **Transactions**
   - Log transaction details (amount, reference, status)

6. **Balance Tracking**
   - Maintain and update user financial records

7. **Search & Filter Options**
   - Search properties and services with specific filters

8. **Notifications**
   - Updates on bookings, transactions, and services

9. **Administrative Dashboard**
   - Monitor platform activity, manage user roles & permissions

---

## 🗄 Database Design

### Key Tables & Attributes
- **User**
  - `id, name, email, password, access_token, role`
- **House List**
  - `serial_number, author, currently_owned_by, image_link, description, price, address, details, type, status`
- **Rent Review**
  - `serial_number, client, comment`
- **Services**
  - `serial_number, service, cost, done_by, status`
- **Transaction**
  - `author, transaction_id, amount, reference, status`
- **User Balance**
  - `author, balance`

### Relationships
- **User → House List** (One-to-Many)
- **User → Rent Review** (One-to-Many)
- **User → Services** (One-to-Many)
- **User → Transactions** (One-to-Many)
- **User → Balance** (One-to-One)

### Data Integrity
- Normalization for data consistency
- Indexes on key fields (`id, email, transaction_id`) for faster queries
- Constraints for foreign keys and uniqueness

---

## ⚙️ Technology Stack

- **Database:** MySQL  
- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** PHP  
- **Server-Side Logic:** PHP + MySQL  

---

## ⚠️ Limitations
- No 3D property models or virtual tours  
- Limited search filters (room count, floor number, size)  
- No bank or mobile payments support  
- No personalized recommendations  
- No rent payment tracking  

---

## 🔮 Future Work

### 🏠 Simplify Searching
- Sort by price, rooms, size, proximity to shops/schools  
- Advanced filters (pool, gym, pet-friendly, elevator, etc.)  
- Keyword search (e.g., *"near park"*)  

### 🎥 Enhance Experience
- 3D tours and virtual walkthroughs  

### 💳 Simplify Payments
- Direct bank & mobile payments (Google Pay, Apple Pay, etc.)  
- Installment options  

### 🤖 Personalized Assistance
- AI-powered property recommendations  
- User profiles with saved preferences  
- Notifications for new matches  

### 📊 Better Rent Management
- Rent payment tracking, reminders, and receipts  

### 🔐 Stronger Security
- Advanced protection against hacking  
- Secure personal data handling  

### 🛠 Extra Features
- Landlord tools for managing properties  
- Built-in chat between tenants and landlords  

---

## ✅ Conclusion
Dream Nest aims to **simplify real estate management** by providing a centralized platform for buying, renting, and managing homes.  
Currently, users can:
- Register accounts
- List properties
- Manage transactions and balances  

With future improvements such as **advanced search, 3D models, better payments, and AI-driven recommendations**, Dream Nest will become a **powerful hub for renters, buyers, and property owners**.

---

## 📌 ER Diagram
*(Add your ER diagram image here when available)*  
```markdown
![ER Diagram](link-to-your-er-diagram.png)
