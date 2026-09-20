# TravelStay 🏡

A full-stack **Airbnb-inspired accommodation web application** built with Node.js, Express.js, MongoDB, and EJS. TravelStay allows users to explore property listings, create and manage their own listings, leave reviews, and authenticate through a server-rendered web interface.

> **Note:** This project is built for learning and portfolio purposes and is inspired by the core functionality of platforms like Airbnb.

## 🚀 Features

* User **signup, login, and logout**
* Create, view, edit, and delete property listings
* Upload and manage listing images using **Cloudinary**
* Add and delete reviews for listings
* Server-side validation for listings and reviews
* Flash messages for user feedback
* Authentication and authorization using sessions
* MongoDB-based data persistence
* Centralized error handling using a custom `ExpressError` class
* Responsive EJS-based user interface
* MVC-style project structure for better code organization

## 🛠️ Tech Stack

**Frontend**

* HTML
* CSS
* JavaScript
* EJS
* Bootstrap

**Backend**

* Node.js
* Express.js
* Express Session
* Connect-Mongo

**Database & Storage**

* MongoDB
* MongoDB Atlas
* Cloudinary

**Other**

* Passport.js
* Joi
* Method-Override
* EJS-Mate

## 📂 Project Structure

```text
TravelStay/
│
├── controllers/
│   ├── listings.js
│   ├── reviews.js
│   └── users.js
│
├── models/
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── routes/
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── views/
│   ├── includes/
│   ├── layouts/
│   ├── listings/
│   └── users/
│
├── public/
│   ├── css/
│   └── js/
│
├── utils/
│   ├── ExpressError.js
│   └── wrapAsync.js
│
├── middleware.js
├── schema.js
├── cloudConfig.js
├── app.js
├── package.json
└── .gitignore
```

## 🔐 Authentication & Authorization

TravelStay uses session-based authentication to manage logged-in users.

Authenticated users can manage their own listings, while authorization middleware prevents users from modifying listings or reviews that they do not own.

Sessions are stored in MongoDB using `connect-mongo`.

## 🖼️ Image Uploads

Listing images are uploaded and stored using **Cloudinary** rather than being stored directly inside the application.

Cloudinary configuration is kept outside the source code using environment variables.

## 🗄️ Database

The application uses **MongoDB** for storing:

* User accounts
* Property listings
* Reviews
* Session data

MongoDB Atlas can be used as the cloud database for deployment.

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Kshitij-Saxena-20/TravelStay.git
cd TravelStay
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create a `.env` file

Create a `.env` file in the project root:

```env
ATLASDB_URL=your_mongodb_connection_string
SECRET=your_session_secret

CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret
```

> Never commit your `.env` file or expose your database and Cloudinary credentials publicly.

### 4. Start the application

```bash
node app.js
```

For development, you can use:

```bash
nodemon app.js
```

The application will run locally on the configured port.

## 🌐 Deployment

The application is designed to be deployed using services such as **Render**, with:

* MongoDB Atlas for the database
* Cloudinary for image storage
* Environment variables for sensitive credentials

## 📚 What I Learned

Building TravelStay helped me gain practical experience with:

* Designing RESTful routes using Express.js
* Building MVC-based Node.js applications
* MongoDB schema design and relationships
* Authentication and authorization
* Session management
* Middleware development
* Server-side rendering with EJS
* Image uploads with Cloudinary
* Form validation
* Error handling in Express
* Git and GitHub workflow
* Preparing a Node.js application for cloud deployment

## 🔮 Future Improvements

Some features that could be added in future versions include:

* Search and filtering of listings
* Map-based location visualization
* Advanced sorting and pagination
* Improved responsive UI
* Booking and reservation functionality
* User profile management
* More comprehensive automated testing

## 👨‍💻 Author

**Kshitij**

B.Tech CSE | Java & DSA | Full-Stack Development

GitHub:
https://github.com/Kshitij-Saxena-20

---

⭐ If you find this project useful or interesting, feel free to explore the repository.
