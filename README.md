# House Rental Management System

A Django-based web application for managing rental properties, connecting landlords and tenants.

## Features
- User authentication (Landlord, Tenant, Admin).
- Property listing, search, and booking.
- Tenant applications and lease agreement generation.
- Payment processing (simulated).
- AI-powered property recommendations.
- Landlord-tenant messaging.

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd house_rental_system
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Setup PostgreSQL**:
   - Install PostgreSQL and create a database named `rental_db`.
   - Update `house_rental/settings.py` with your database credentials.

5. **Run migrations**:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Load sample data**:
   ```bash
   python manage.py loaddata properties/fixtures/sample_data.json
   ```

7. **Create a superuser**:
   ```bash
   python manage.py createsuperuser
   ```

8. **Run the server**:
   ```bash
   python manage.py runserver
   ```

9. **Access the app**:
   - Open `http://localhost:8000` in your browser.
   - Admin panel: `http://localhost:8000/admin`.

## Credentials
- Landlord: `landlord1` / `password123`
- Tenant: `tenant1` / `password123`

## Deployment
- Use Heroku, AWS, or DigitalOcean with Gunicorn and Nginx.
- Set environment variables for `SECRET_KEY`, database credentials, and `DEBUG=False`.

## Future Enhancements
- Integrate Stripe for real payment processing.
- Add AI chatbots with Django Channels.
- Implement blockchain-based smart contracts.
