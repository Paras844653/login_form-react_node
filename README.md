# Node.js & React User Authentication System

A simple yet powerful User Authentication system built with **Node.js** on the backend and **React.js** on the frontend. This project allows users to log in, register, and manage their accounts, all with robust functionality including OTP (One-Time Password) verification and account deletion.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Backend Setup](#backend-setup)
- [Frontend Setup](#frontend-setup)
- [Usage](#usage)
- [Routes](#routes)
- [License](#license)

---

## Project Overview

This is a **User Authentication System** where users can:

- **Log in** using their credentials.
- **Register** for a new account.
- Receive and verify an **OTP** (One-Time Password).
- **View account details** post-login.
- **Delete their account** from the system.

Built using **Node.js** and **React.js**, this project is intended to be simple yet robust, with features like form validation, JWT-based authentication, and user account management.

---

## Features

### **User Login**
- Users can log in using their email and password.
- Credentials are validated against the database.
- If successful, an **OTP** is sent for extra security.
- After OTP verification, the user is redirected to a **Thank You Page** showing their account details.

### **User Registration**
- Users can create an account by providing necessary information: name, email, password, company name, age, DOB, and profile image (PNG/JPG).
- Email validation and password case-sensitivity are enforced.

### **OTP Verification**
- After login, a **6-digit OTP** is generated and sent to the user.
- OTP is valid for 10 minutes and must be entered correctly to continue.

### **Account Management**
- Users can **delete their account** via the "Thank You" page.
- Account details are displayed post-login for easy access.

---

## Technologies Used

- **Frontend**: React.js, Axios
- **Backend**: Node.js, Express.js, MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **File Upload**: Multer (for image storage)
- **Styling**: Custom CSS for responsiveness

---

## Installation

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/user-authentication.git
    ```

2. Navigate to the backend folder:
    ```bash
    cd backend
    ```

3. Install the dependencies:
    ```bash
    npm install
    ```

4. Create a `.env` file in the root directory with the following variables:
    ```bash
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret_key
    ```

5. Start the server:
    ```bash
    npm run dev
    ```

   The backend will now be running on **http://localhost:5000**.

---

### Frontend Setup

1. Navigate to the frontend folder:
    ```bash
    cd frontend
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Start the React app:
    ```bash
    npm start
    ```

   The frontend will now be available at **http://localhost:3000**.

---

## Usage

1. Open the app in your browser at **http://localhost:3000**.
2. Use the **Login** form to enter your credentials or click on **Create Account** to register a new user.
3. After logging in, check your email for an OTP. Enter the OTP on the **OTP Verification** page.
4. Once verified, you will be redirected to the **Thank You Page** with your account details.

---

## Routes

### **Backend Routes**

- **POST /api/auth/login** - Logs in a user with email and password.
- **POST /api/auth/verify-otp** - Verifies the OTP entered by the user.
- **POST /api/auth/register** - Registers a new user.
- **DELETE /api/user/delete** - Deletes the user account.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Screenshots

### **Login Page**
![Login](./screenshots/login.png)

### **OTP Verification Page**
![OTP Verification](./screenshots/otp-verification.png)

### **Thank You Page**
![Thank You](./screenshots/thank-you.png)

---

## Future Enhancements

- **Password Reset**: Add functionality to reset forgotten passwords.
- **Rate Limiting**: Implement rate limiting to prevent abuse of the OTP verification system.
- **User Profile**: Allow users to update their profile information.

---

## Contributing

If you'd like to contribute to this project, please fork the repository, make your changes, and submit a pull request. Contributions are welcome!

---

## Acknowledgements

- Thanks to **Express.js**, **MongoDB**, **React**, and **JWT** for providing easy-to-use solutions for building web applications.

---

Feel free to modify the **README** as needed. Enjoy working on the project!
