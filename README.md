# E-commerce Site

A Django-based e-commerce website with product management, user authentication, and shopping cart functionality.

## Technology Stack

- **Backend**: Django 4.2
- **Frontend**: HTML, CSS, JavaScript
- **Database**: SQLite (development), PostgreSQL (production)
- **Authentication**: Django's built-in authentication system
- **Static Files**: Django's static files handling
- **Media Files**: Django's media files handling

## Features

### User Features
- User authentication (login, register, logout)
- User profile management
- Password reset functionality
- Order history tracking

### Product Features
- Product listing with categories
- Product search functionality
- Product details with images
- Product reviews and ratings
- Product filtering and sorting

### Shopping Features
- Shopping cart functionality
- Checkout process
- Order tracking
- Payment integration

### Payment integration
-Multiple payment options:
  - UPI Payment
  - Cash on Delivery (COD)

### Admin Features
- Admin panel for product management
- Order management
- User management
- Category management
- Sales reports

## API Endpoints

### Authentication
- `/accounts/login/` - User login
- `/accounts/register/` - User registration
- `/accounts/logout/` - User logout
- `/accounts/password-reset/` - Password reset

### Products
- `/products/` - List all products
- `/products/<id>/` - Product details
- `/products/category/<category>/` - Products by category
- `/products/search/` - Search products

### Cart
- `/cart/` - View cart
- `/cart/add/<product_id>/` - Add to cart
- `/cart/remove/<product_id>/` - Remove from cart
- `/cart/update/<product_id>/` - Update cart quantity

  # E-commerce Site

A Django-based e-commerce website with product management, user authentication, and shopping cart functionality.

## Features

### User Features
- User authentication (login, register, logout)
- User profile management
- Password reset functionality
- Order history tracking

### Product Features
- Product listing with categories
- Product search functionality
- Product details with images
- Product reviews and ratings
- Product filtering and sorting

### Shopping Features
- Shopping cart functionality
- Wishlist
- Checkout process
- Order tracking
- Payment integration

### Admin Features
- Admin panel for product management
- Order management
- User management
- Category management
- Sales reports

## Screenshots

### Home Page
![image](https://github.com/user-attachments/assets/e8aa058a-6a0c-4fe5-bcfb-f56dbfa048d4)


### Product Listing
![image](https://github.com/user-attachments/assets/e0392da4-2e97-49c4-ada0-99e6b8bb33ec)


### Product Details
![image](https://github.com/user-attachments/assets/43713f99-3304-4b3b-90a8-43110f33e656)


### Shopping Cart
![image](https://github.com/user-attachments/assets/f3aec47e-e849-4c07-9c72-e64332ee6761)


### User Dashboard
![image](https://github.com/user-attachments/assets/c807e344-2e30-4ace-87da-1290089df543)


### Payment Page
![image](https://github.com/user-attachments/assets/e9b443e5-21df-4557-a781-f1e6577dc1ce)


### Admin Panel
![image](https://github.com/user-attachments/assets/71afc447-7bea-4afc-b14e-d85cfdabb7b9)


// ... existing code ...

## Setup Instructions

1. Clone the repository:
```bash
git clone <your-repository-url>
cd ecommerce_site
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
   - Copy `ecommerce_site/sample_settings.py` to `ecommerce_site/local_settings.py`
   - Update the settings in `local_settings.py` with your configuration

5. Run migrations:
```bash
python manage.py migrate
```

6. Create a superuser:
```bash
python manage.py createsuperuser
```

7. Collect static files:
```bash
python manage.py collectstatic
```

8. Run the development server:
```bash
python manage.py runserver
```

9. Visit http://localhost:8000 in your browser

## Project Structure

- `ecommerce_site/` - Main project directory
  - `settings.py` - Project settings
  - `urls.py` - Main URL configuration
  - `wsgi.py` - WSGI configuration
  - `asgi.py` - ASGI configuration
- `shop/` - Main application directory
  - `models.py` - Database models
  - `views.py` - View functions
  - `urls.py` - URL patterns
  - `forms.py` - Form definitions
  - `admin.py` - Admin configurations
- `static/` - Static files (CSS, JS, images)
- `media/` - User-uploaded files
- `templates/` - HTML templates
- `requirements.txt` - Project dependencies
- `manage.py` - Django management script

## Troubleshooting

### Common Issues

1. **Static Files Not Loading**
   - Run `python manage.py collectstatic`
   - Check `STATIC_ROOT` and `STATIC_URL` in settings
   - Ensure `django.contrib.staticfiles` is in `INSTALLED_APPS`

2. **Media Files Not Uploading**
   - Check `MEDIA_ROOT` and `MEDIA_URL` in settings
   - Ensure media directory exists and has proper permissions

3. **Database Issues**
   - Delete `db.sqlite3` and run migrations again
   - Check database settings in `local_settings.py`

4. **Template Not Found**
   - Check template directory structure
   - Verify template name in view
   - Ensure app is in `INSTALLED_APPS`

### Development Tips

1. **Debug Mode**
   - Set `DEBUG = True` in `local_settings.py` for development
   - Never enable debug mode in production

2. **Secret Key**
   - Keep your secret key secure
   - Use environment variables in production

3. **Database**
   - Use SQLite for development
   - Use PostgreSQL for production

## Contributing

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request


## Contact

For any questions or issues, please open an issue in the GitHub repository.
