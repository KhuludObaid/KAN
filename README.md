# 🌐 KFUPM Activity Network (KAN)

## 📘 Project Description

**KFUPM Activity Network** is a full-stack web platform designed to help students discover, register, and engage with university events and clubs. It allows for role-based interaction between students, club administrators, and system administrators.

Key features include:

- 🔗 Social media integration  
- 📝 Event registration  
- 🌑 Dark mode  
- 📊 Role-based dashboards (Admin, Club Admin, Student)  
- 🧾 Ticket generation and QR scanning  
- 📥 Club membership application & review  
- 🛡️ Backend validation and duplicate protection  

---

## ⚙️ Setup and Installation Instructions

### ✅ Prerequisites

Ensure the following are installed:

- 🟢 **Node.js** – [Download Node.js](https://nodejs.org/)
- 🧰 **Git** – Version control system
- 🟠 **MongoDB** – For backend data storage (local or cloud via Atlas)

---

### 📁 Clone the Repository

```bash
git clone https://github.com/funoonAlbalawi12/SWE363Project.git
cd SWE363Project
```

---

### 🖥️ Frontend Setup

```bash
cd frontend
npm install
npm start
```

---

### 🛠️ Backend Setup

```bash
cd ../backend
npm install
npm run dev
```

> 🔒 Create a `.env` file in the backend directory with the following:
```env
PORT=5001
MONGO_URI=your_mongodb_connection_string
STRIPE_SECRET_KEY=your_stripe_secret_key
```

---

## 🚀 Usage Instructions

Users are redirected based on their roles:

### 👤 Admin
- Manage clubs, events, and user roles  
- Approve or reject club requests  

### 🧑‍💼 Club Admin
- Create and manage events  
- View registered members  
- Post announcements  

### 👨‍🎓 Student
- Register for events  
- View and manage tickets  
- Apply to join clubs  

---

## 🧱 Tech Stack

- **Frontend**: React.js, CSS, React Router, Axios  
- **Backend**: Node.js, Express.js, MongoDB, Mongoose, Stripe  
- **Tools**: GitHub, VS Code, Figma  
- **Features**: REST API, JWT authentication, QR code ticketing, dark mode  

---

## 🖌️ Figma Design

🎨 [View on Figma](https://www.figma.com/proto/qtgg5Tq9rN33B2dAEuZiSH/swe363-project-KAN-?node-id=0-1&t=ii6pirTXHxPRfdzG-1)

---

## 👥 Team Members

| Name              | Role Description |
|-------------------|------------------|
| **Funoon Albalawi** | Admin dashboard & management logic |
| **Budoor Alshehri** | Admin UX/UI and system integration |
| **Khulud Alotaibi** | Student dashboard, homepage, and event registration |
| **Zahra Alhadab** | Club Admin interface: event & announcement control |
| **Rahf Altwairqi** | Club Admin interface: member & event management |
---

## 🧾 How to Register

### 👨‍🎓 Student Registration
- Visit the homepage and click on **Explore Events**.
- Register for an event with your name and email to create a student account.

### 🧑‍💼 Club Admin Registration
- A club admin account is created when a user applies to join a club and is approved by the system admin.
- After approval, the user gains access to the club admin dashboard.

### 👤 Admin Access
- Admin credentials are preconfigured or manually created in the database.
- Admin users can log in directly to access system-wide management features.

---

## 📡 API Endpoints

| Method | Endpoint                          | Description                              |
|--------|-----------------------------------|------------------------------------------|
| GET    | `/api/users/test`                 | Test API connectivity                    |
| POST   | `/api/users/register`             | Register a user                          |
| POST   | `/api/users/login`                | Log in a user                            |
| GET    | `/api/events`                     | Fetch all events                         |
| POST   | `/api/events`                     | Create a new event (Club Admin)          |
| GET    | `/api/tickets/:userId`            | Get all tickets for a user               |
| POST   | `/api/tickets/register`           | Register for a ticket                    |
| GET    | `/api/clubs`                      | Get all clubs                            |
| POST   | `/api/clubs`                      | Create a new club                        |
| POST   | `/api/clubmemberships/apply`      | Student applies to join a club           |
| GET    | `/api/clubmemberships/:clubId`    | Get all club membership requests         |
| POST   | `/api/eventregistrations`         | Register a student for an event          |
| POST   | `/api/payments/checkout-session`  | Create Stripe checkout session           |

---

## 📁 Project Structure

```
SWE363Project/
│
├── frontend/               # React frontend
│   ├── src/
│   └── public/
│
├── backend/                # Node.js backend
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── config/
│   └── server.js
```

---

## 🧪 Running Tests

To run backend tests (if implemented):

```bash
cd backend
npm test
```

---

## 🌍 Deployment

Frontend: [https://your-frontend-link](#)  
Backend API: [https://your-backend-link](#)
---

## 🧪 Demo User Accounts

Use the following credentials to log in for testing purposes:

| Role    | Email               | Password   |
|---------|---------------------|------------|
| Student | khulud@outlook.com  | 12345678   |
| Admin   | budoor@outlook.com  | admin123   |
| club admin   | rahf@outlook.com  | clubadmin   |
> ⚠️ These accounts are for demo/testing only. Do **not** use real passwords or emails in production.
