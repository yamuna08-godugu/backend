# Expense Tracker - Backend

This is the backend service for the Expense Tracker Application. It provides a RESTful API to manage expense records, using Node.js, Express, and MongoDB.

## 📋 Features

- Add a new expense
- Retrieve all expenses
- Update an existing expense
- Delete an expense
- (Optional) User authentication for multiple users

##  Technologies Used

- Node.js
- Express.js
- (Optional) JSON Web Tokens (JWT) for authentication
- dotenv for environment variables
- cors and body-parser middleware

##  Getting Started

Follow these steps to set up the backend locally:

1. Clone the repository:

   ```bash
   https://github.com/yamuna08-godugu/backend.git
   
Navigate to the backend directory:

bash
Copy
Edit
cd backend
Install dependencies:

bash
Copy
Edit
npm install
Set up environment variables:

Create a .env file in the /backend folder and add:

ini
Copy
Edit
PORT=5000
MONGO_URI=your_mongodb_connection_string
Start the server:

bash
Copy
Edit
node server.js
Or, for auto-reloading:

bash
Copy
Edit
npm install -g nodemon
nodemon server.js
The server will start at:

arduino
Copy
Edit
http://localhost:5000

API Endpoints
Add Expense
POST /expenses

Request body:

json
Copy
Edit
{
  "amount": 100,
  "category": "Food",
  "description": "Lunch",
  "date": "2025-04-27"
}
Get All Expenses
GET /expenses

Update Expense
PUT /expenses/:id

Request body:

json
Copy
Edit
{
  "amount": 120,
  "category": "Food",
  "description": "Updated Lunch",
  "date": "2025-04-27"
}
Delete Expense
DELETE /expenses/:id

Project Structure
bash
Copy
Edit
/backend
 ├── models/
 │    └── Expense.js
 ├── routes/
 │    └── expenses.js
 ├── server.js
 └── .env
models/Expense.js: Mongoose model for expense records

routes/expenses.js: Route handlers for expense operations

server.js: Main server file (Express app setup)
