# Django Authentication with Allauth

This repository contains a Django project that implements user authentication using Django Allauth. The project includes features such as user login, signup, logout, and integration with third-party providers like Google.

## Features

- User Signup and Login
- Logout functionality
- Password reset and change
- Social authentication with Google
- Customizable user authentication flow

## Installation

To get started with this project, follow the steps below:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/diyorbekqodirboyev863/dj-authentication.git
   cd dj-authentication
   ```

2. **Create a virtual environment:**

   ```bash
   python -m venv env
   ```

3. **Activate the virtual environment:**

   - On Windows:
     ```bash
     .\env\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source env/bin/activate
     ```

4. **Install the required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

5. **Set up the database:**

   Run the migrations to create the necessary database tables:

   ```bash
   python manage.py migrate
   ```

6. **Create a superuser:**

   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server:**

   ```bash
   python manage.py runserver
   ```

8. **Access the application:**

   Open your browser and go to `http://127.0.0.1:8000/` to see the application in action.

## Configuration

### Google OAuth

To enable Google authentication, you need to set up Google OAuth credentials:

1. Create a project in [Google Cloud Console](https://console.cloud.google.com/).
2. Enable OAuth 2.0 and create credentials for a web application.
3. Add the client ID and secret to your `settings.py`:

   ```python
   SOCIALACCOUNT_PROVIDERS = {
       'google': {
           'APP': {
               'client_id': 'YOUR_GOOGLE_CLIENT_ID',
               'secret': 'YOUR_GOOGLE_CLIENT_SECRET',
               'key': ''
           }
       }
   }
   ```

4. Update the `ALLOWED_HOSTS` and `SITE_ID` in `settings.py` accordingly.

## Usage

- **Signup:** Go to `/accounts/signup/` to create a new account.
- **Login:** Go to `/accounts/login/` to log in to an existing account.
- **Logout:** Use the `/accounts/logout/` endpoint to log out.
- **Google Login:** Use the Google login button on the login page to authenticate via Google.

## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request.
