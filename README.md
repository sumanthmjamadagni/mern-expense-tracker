# Expense Tracker - MERN Stack Application

A full-stack expense tracker application built with MongoDB, Express.js, React.js, and Node.js (MERN Stack) featuring Framer Motion animations and MongoDB Atlas integration.

## Features

- 💰 Add Income and Expenses with separate buttons
- 📊 Real-time Total Balance calculation
- 🎨 Beautiful UI with Framer Motion animations
- 📱 Responsive design for mobile and desktop
- 🗂️ Category-based transaction organization
- 📅 Date tracking for all transactions
- ❌ Delete transactions functionality
- ☁️ Cloud-based storage with MongoDB Atlas

## Tech Stack

- **Frontend**: React.js, Framer Motion, Axios
- **Backend**: Node.js, Express.js
- **Database**: MongoDB Atlas
- **Styling**: CSS3 with modern gradients and animations

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB Atlas account
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd expense-tracker-mern
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd client
   npm install
   cd ..
   ```

4. **Configure MongoDB Atlas**
   - Create a MongoDB Atlas account at https://www.mongodb.com/atlas
   - Create a new cluster
   - Get your connection string
   - Update the `.env` file with your MongoDB URI:
   ```
   MONGODB_URI=mongodb+srv://your-username:your-password@cluster0.mongodb.net/expense-tracker?retryWrites=true&w=majority
   PORT=5000
   JWT_SECRET=your-jwt-secret-key
   ```

5. **Run the application**
   
   **Development mode (runs both frontend and backend):**
   ```bash
   npm run dev
   ```
   
   **Or run separately:**
   
   Backend only:
   ```bash
   npm run server
   ```
   
   Frontend only:
   ```bash
   npm run client
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## API Endpoints

- `GET /api/transactions` - Get all transactions
- `POST /api/transactions` - Create new transaction
- `DELETE /api/transactions/:id` - Delete transaction
- `GET /api/transactions/balance` - Get balance summary

## Project Structure

```
expense-tracker-mern/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── Home.js
│   │   │   └── AddTransaction.js
│   │   ├── App.js
│   │   └── App.css
├── models/
│   └── Transaction.js      # MongoDB schema
├── routes/
│   └── transactions.js     # API routes
├── server.js              # Express server
├── package.json
└── .env                   # Environment variables
```

## Usage

1. **Home Page**: View your total balance, income, and expenses
2. **Add Income**: Click the "Add Income" button to record income
3. **Add Expense**: Click the "Add Expense" button to record expenses
4. **View Transactions**: See all transactions with delete functionality
5. **Real-time Updates**: Balance updates automatically when adding/deleting transactions

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.