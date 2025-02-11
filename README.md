Contact Management API

This is a simple Contact Management API built using Node.js, Express.js, and MongoDB. It allows users to create, read, update, and delete (CRUD) contacts.

Features:

1.Fetch all contacts
2.Create a new contact
3.Update an existing contact
4.Delete a contact
5.Fetch a single contact by ID
6.Data validation using express-validator
7.Error handling with proper HTTP status codes

Technologies Used:

1.Node.js
2.Express.js
3.MongoDB with Mongoose
4.Express Validator
5.Dotenv

Setup Instructions:

1. Clone the repository:

 git clone https://github.com/saifullahali2000/blackwinstech.git
 cd contact-management-api

2. Install Dependencies:

npm install


4. Start the Server:

npm start  # or nodemon server.js

API Endpoints:

1. Get All Contact:

GET /api/contacts

Response:

[
  {
    "_id": "650c3b8e7d2b3a001fa7c123",
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890",
    "address": "123 Main St",
    "createdAt": "2024-02-10T10:00:00.000Z"
  }
]

2. Get Contact by ID:

GET /api/contacts/:id

Response:

{
  "_id": "650c3b8e7d2b3a001fa7c123",
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "1234567890",
  "address": "123 Main St",
  "createdAt": "2024-02-10T10:00:00.000Z"
}

3. Create a Contact:

POST /api/contacts

Request Body:

{
  "name": "Alice Smith",
  "email": "alice@example.com",
  "phone": "9876543210",
  "address": "456 Elm St"
}

Response:

{
  "_id": "650c3b8e7d2b3a001fa7c124",
  "name": "Alice Smith",
  "email": "alice@example.com",
  "phone": "9876543210",
  "address": "456 Elm St",
  "createdAt": "2024-02-10T10:05:00.000Z"
}

4. Update a Contact:

PUT /api/contacts/:id

Request Body:

{
  "name": "Alice Johnson",
  "email": "alicej@example.com",
  "phone": "9876543210",
  "address": "789 Pine St"
}

Response:

{
  "_id": "650c3b8e7d2b3a001fa7c124",
  "name": "Alice Johnson",
  "email": "alicej@example.com",
  "phone": "9876543210",
  "address": "789 Pine St",
  "createdAt": "2024-02-10T10:05:00.000Z"
}

5. Delete a Contact:

DELETE /api/contacts/:id

Response:

{
  "message": "Contact deleted successfully"
}

Error Handling:

Returns 400 Bad Request for missing required fields.
Returns 404 Not Found if the contact does not exist.
Returns 500 Internal Server Error for server issues.

License:

This project is open-source and free to use.

