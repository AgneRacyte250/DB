# DB
# HousingProject

## Overview

HousingProject is a web application designed to perform CRUD operations on housing data. It features user authentication and authorization, allowing only authenticated users to access certain functionalities. 
The backend is built with Node.js, Express, and MongoDB, while the frontend is developed using Angular.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Technologies](#technologies)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication (signup, signin, signout)
- JWT-based authorization
- Session handling with `express-session` and `connect-mongo`
- CRUD operations for housing data
- Secure password storage with bcrypt

## Installation

### Prerequisites

- Node.js
- MongoDB

### Backend Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/AgneRacyte250/HousingProject.git
    ```

2. Navigate to the backend directory:
    ```sh
    cd HousingProject/Back_End
    ```

3. Install dependencies:
    ```sh
    npm install
    ```

4. Run the server:
    ```sh
    node server.js
    ```

### Frontend Setup

1. Navigate to the Front_End directory:
    ```sh
    cd ../Front_End
    ```

2. Install dependencies:
    ```sh
    npm install
    ```

3. Run the frontend server:
    ```sh
    ng serve
    ```

## Usage

Once the backend and frontend servers are running, you can access the application at `http://localhost:4200`.

### User Authentication

- **Signup**: Create a new user account.
- **Signin**: Login with your credentials to receive an access token.
- **Signout**: Logout from the application, destroying the session.

### Housing Data Operations

- **Create**: Add new housing data.
- **Read**: View existing housing data.
- **Update**: Modify existing housing data.
- **Delete**: Remove housing data.

## Project Structure

```plaintext
HousingProject/
│
├── Back_end/
│   ├── src/
│   │   ├── controller/
│   │   │   ├── authController.js
│   │   │   └── housingController.js
│   │   ├── middleware/
│   │   │   └── sessionMiddleware.js
│   │   ├── models/
│   │   │   ├── userModel.js
│   │   │   └── housingModel.js
│   │   ├── routes/
│   │   │   ├── authRoutes.js
│   │   │   └── housingRoutes.js
│   │   ├── service/
│   │   │   ├── userService.js
│   │   │   └── housingService.js
│   ├── server.js
│   ├── package.json
│   └── package-lock.json
│
└── Front_End/
    ├── src/
    │   ├── app/
    │   │   ├── components/
    │   │   │   ├── housing-create/
    │   │   │   ├── housing-list/
    │   │   │   └── login/
    │   │   ├── services/
    │   │   │   ├── auth.service.ts
    │   │   │   └── housing.service.ts
    │   ├── app.module.ts
    │   ├── app.component.ts
    │   └── app.component.html
    ├── angular.json
    ├── package.json
    └── package-lock.json
