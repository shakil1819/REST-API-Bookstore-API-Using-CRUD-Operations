# Online Bookstore API with Node.js and MongoDB

This project is a RESTful API for an online bookstore built using Node.js and MongoDB. The API allows users to perform CRUD operations for books, search for books by title, author, or genre, add books to a shopping cart, place an order, and view order history.

## Project Structure

```text
.
├── public
│   ├── img
│   │   ├── Book fav.png
│   │   └── logo.png
│   ├── javascript
│   │   ├── admin.js
│   │   ├── adminLogin.js
│   │   └── index.js
│   └── stylesheets
│       ├── 404.css
│       ├── admin-login.css
│       ├── admin.css
│       └── index.css
├── src
│   ├── db
│   │   ├── models
│   │   │   ├── admin.js
│   │   │   ├── book.js
│   │   │   └── user.js
│   │   ├── mongoose.js
│   │   └── routers
│   │       ├── adminRouter.js
│   │       ├── bookRouter.js
│   │       └── userRouter.js
│   ├── index.js
│   ├── middleware
│   │   └── authentication.js
│   └── utils
│       └── SearchFilter.js
├── views
│   ├── 404.hbs
│   ├── admin.hbs
│   ├── adminLogin.hbs
│   └── index.hbs
├── .env
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Installation

### Prerequisites

- Node.js
- MongoDB
- Docker (optional)

### Steps

1. **Clone the repository**

    ```bash
    https://github.com/shakil1819/REST-API-Bookstore-API-Using-CRUD-Operations.git
    cd REST-API-Bookstore-API-Using-CRUD-Operations
    ```

2. **Install Dependencies**

    ```bash
    npm install
    ```

3. **Configure MongoDB**

    Create a `.env` file in the root directory and add the MongoDB connection string:

    ```env
    MONGODB_URI=mongodb://localhost:27017/bookstore
    ```

4. **Build and Run the Application**

    ```bash
    npm start
    ```

    Or using Docker:

    ```bash
    docker-compose up --build
    ```

## Testing

### Postman Collection

A Postman collection is provided to test the API endpoints. Import the `Bookstore API.postman_collection.json` file into Postman to use the collection.

### Testing Steps

1. **Admin Login**

    - **URL:** `http://localhost:3000/admin/login`
    - **Method:** `GET`

2. **Admin Order History**

    - **URL:** `http://localhost:3000/admin/orders`
    - **Method:** `GET`
    - **Headers:** `Authorization: Bearer <Admin_Token>`

3. **Admin Logout**

    - **URL:** `http://localhost:3000/admin/logout`
    - **Method:** `GET`
    - **Headers:** `Authorization: Bearer <Admin_Token>`


