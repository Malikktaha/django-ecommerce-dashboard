# ShopSmart - Django E-commerce Dashboard

**Author:** Taha Nawaz  
**Roll No:** SU92-BSEFM-F24-004  

## Project Overview
ShopSmart is a dynamic e-commerce dashboard built with Django. The application demonstrates Django templates, template inheritance, custom filters and tags, loops, conditionals, and pagination. Users can view products, add them to the cart, and view profile information.

## Features

### Base Template & Includes
- Reusable `header.html` and `footer.html` in `base.html`
- Header: Site name and navigation links (Home, Products, Cart, Profile)
- Footer: Current year and total number of products via a custom template tag

### Home Page
- Welcome message
- Conditional greeting:
  - If authenticated: `Welcome back, {{ user.username }}!`
  - Else: `Sign in to start shopping`

### Products Page
- Products displayed in a grid layout with Name, Price, Stock Status
- Out-of-stock products display **"Out of Stock"**
- Reusable product card included using `{% include %}`
- Pagination using Django’s built-in paginator
- Search functionality to filter products dynamically

### Cart Page
- Displays items in cart
- Calculates total price dynamically

### Profile Page
- Shows username and email of logged-in user
- All pages extend `base.html` using template inheritance

### Custom Filters & Tags
- `price_format` filter: Formats product prices (e.g., 1,200.00)
- `total_products` tag: Returns total number of products in the database

## Project Structure

## Installation & Setup
```bash
git clone <repository-url>
cd shopsmart
python -m venv myenv
# Activate environment
# Windows:
myenv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser  # optional
python manage.py runserver
