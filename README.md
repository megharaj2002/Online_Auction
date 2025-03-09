# Online_Auction

A simple and beginner-friendly auction application built with **React**, **Vite**, **React Router**, and **Express.js**. This app allows users to sign up, sign in, post auctions, place bids, and view auction details.

---

## Key Features
### **1. Authentication**
- **Sign Up**: Users can create an account by providing a username and password. Passwords are securely hashed using **bcryptjs**.
- **Sign In**: Registered users can log in using their credentials. Authentication is handled using **JSON Web Tokens (JWT)**.
- **Log Out**: Users can log out, which clears their session and redirects them to the landing page.
- **Protected Routes**: Only authenticated users can access protected routes like `/dashboard` and `/post-auction`.

### **2. Auction Management**
- **Post Auctions**: Authenticated users can post new auction items with details like:
  - Item Name
  - Description
  - Starting Bid
  - Closing Time
- **View Auctions**: Users can view a list of all active auctions on the dashboard.
- **Place Bids**: Users can place bids on auction items. The bid must be higher than the current bid.
- **Edit Auctions**: Users can edit the details of their posted auctions (e.g., item name, description, closing time).
- **Delete Auctions**: Users can delete their posted auctions.

### **3. Error Handling**
- Displays error messages for invalid inputs (e.g., missing fields, invalid credentials).
- Shows alerts for API errors (e.g., failed to post auction, bid too low).

### **4. Loading States**
- Displays loading indicators while:
  - Fetching auction items.
  - Posting a new auction.
  - Placing a bid.

### **5. Responsive Design**
- The app is designed to work seamlessly on both desktop and mobile devices.
- Basic styling with **plain CSS** ensures a clean and user-friendly interface.

### **6. Currency and Date Format**
- **Currency**: All monetary values are displayed in **Indian Rupees (₹)**.
- **Date and Time**: Dates and times are displayed in **Indian Standard Time (IST)**.

### **7. Database Integration**
- **MongoDB**: Used to store user data and auction details.
- **Mongoose**: Simplifies MongoDB object modeling and provides schema validation.

### **8. Real-Time Updates**
- Users can view real-time updates on bids and auction status (e.g., highest bidder, current bid).

### **9. User-Friendly Interface**
- **Labels**: All input fields in the **Post Auction** page have clear labels.
- **Dashboard**: Displays auction items in an organized manner with details like:
  - Item Name
  - Current Bid
  - Highest Bidder
  - Closing Time

### **10. Security**
- **Password Hashing**: Passwords are securely hashed using **bcryptjs**.
- **JWT Authentication**: Ensures secure user authentication and session management.
---

## Technologies Used

- **Frontend**:
  - React
  - Vite (for fast development and builds)
  - React Router (for routing)
  - Axios (for API requests)
- **Backend**:
  - Express.js
  - MongoDB (for database)
  - Mongoose (for MongoDB object modeling)
  - bcryptjs (for password hashing)
  - jsonwebtoken (for authentication)
---

## Setup Instructions

### Prerequisites

- Node.js (v16 or higher)
- npm (comes with Node.js)
- MongoDB (running locally or remotely)

### Steps to Run the Project

1. **Clone the Repository**:
   
2. **Install Dependencies**:
   - For the frontend:
     ```bash
     cd frontend
     npm install
     ```
   - For the backend:
     ```bash
     cd backend
     npm install
     ```

3. **Start the Backend Server**:
   - Navigate to the `backend` directory:
     ```bash
     cd backend
     npm run dev
     ```
   - The backend will run at `http://localhost:5001`.

4. **Start the Frontend Development Server**:
   - Navigate to the `frontend` directory:
     ```bash
     cd frontend
     npm run dev
     ```
   - The frontend will run at `http://localhost:5173`.

5. **Open the App**:
   - Access the app at `http://localhost:5173`.

---

## Project Structure

```
EY_GDS-Intenrship-MERN/
├── backend/
│   ├── config/
│   │   └── dbconfig.js
│   ├── db/
│   │   └── db.js
│   ├── middleware/
│   │   └── authenticate.js
│   ├── models/
│   │   └── models.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── auctionRoutes.js
│   │   └── bidRoutes.js
│   ├── server.js
│   ├── .env
│   └── package.json
│
├── frontend/
│   ├── public/
│   │   ├── favicon.jpg
│   │   └── favicon.ico
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Landing.jsx
│   │   │   ├── Signup.jsx
│   │   │   ├── Signin.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── AuctionItem.jsx
│   │   │   ├── ProtectedRoute.jsx
│   │   │   └── PostAuction.jsx
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
├── Results/
│   ├── Screenshot_Home.png
│   ├── Screenshot_SignUp.png
│   ├── Screenshot_SignIn.png
│   ├── Screenshot_PostAuction.png
│   ├── Screenshot_Dashboard.png
│   
├── Megharaja_A_N.pptx
└── README.md
```

---

## Screenshots

### Landing Page
![Landing Page](/Results/Screenshot_Home.png)

### SignUp Page
![SignUp Page](/Results/Screenshot_SignUp.png)

### SignIn Page
![SignIn Page](/Results/Screenshot_SignIn.png)

### Post Auction Page
![Post Auction](/Results/Screenshot_PostAuction.png)

### Dashboard Page
![Dashboard](/Results/Screenshot_Dashboard.png)




---

## Future Enhancements**
- **Payment Integration**: Allow users to make payments for winning bids.
- **Advanced Search**: Add filters for searching auction items (e.g., by category, price range).
- **Multi-Language Support**
---

