# Flask Auth0 Login Demo

## Overview

This project demonstrates how to integrate Auth0 authentication into a Flask web application. It includes secure login, logout, and a protected route accessible only to authenticated users.

## Features

* Login via Auth0
* Logout securely
* Protected route `/protected`
* Session-based authentication

## Requirements

* Python 3.x
* Auth0 account
* Git

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Keval0045/Auth0-lab-python.git
cd flask-auth0-login-demo
```

### 2. Create and Activate Virtual Environment (Recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # For Mac/Linux
# OR
venv\Scripts\activate  # For Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Auth0

Login to your [Auth0 Dashboard](https://manage.auth0.com/):

* Go to **Applications > Your App > Settings**
* Set **Allowed Callback URLs** to:

```
http://localhost:3000/callback
```

* Set **Allowed Logout URLs** to:

```
http://localhost:3000
```

* Note down:

  * Domain
  * Client ID
  * Client Secret

### 5. Configure Environment Variables

Create a `.env` file:

```ini
AUTH0_CLIENT_ID=YourAuth0ClientID
AUTH0_CLIENT_SECRET=YourAuth0ClientSecret
AUTH0_DOMAIN=YourAuth0Domain
APP_SECRET_KEY=GenerateWithOpenssl
PORT=3000
```

Generate `APP_SECRET_KEY` using:

```bash
openssl rand -hex 32
```

### 6. Run the App

```bash
python3 server.py
```

App runs at [http://localhost:3000](http://localhost:3000)

## File Structure

```
project-root/
│
├── server.py
├── .env
├── requirements.txt
├── templates/
│   ├── home.html
│   └── dashboard.html (optional)
```

## Demo Video

https://youtu.be/gyxH3wZKKQ4

## What I Learned

* How to integrate Auth0 with Flask
* Managing sessions and protected routes
* Using `.env` securely

## Author

Keval Trivedi
GitHub: [Keval0045](https://github.com/Keval0045)

---

Feel free to fork and build upon this project.
