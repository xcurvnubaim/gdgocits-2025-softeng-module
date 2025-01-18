Here's a breakdown of how to create a simple e-commerce website using HTML, CSS, and JavaScript:

---

### Step 1: Set Up the HTML File

The HTML file is the backbone of the website, defining its structure and content. In this example, the file is named **`Toko.html`**, and it integrates Bootstrap for responsive styling and FontAwesome for icons.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EasyGoin by Augista</title>

    <!-- CSS -->
    <link rel="stylesheet" type="text/css" href="tokoelektro.css">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- FontAwesome -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.1/css/all.min.css" rel="stylesheet">
</head>
<body>
<!-- Navbar Header -->
<header>
    <nav class="navbar navbar-expand-lg navbar-light bg-dark">
        <div class="container">
            <a class="navbar-brand" href="Toko.html">
                <img src="img/LOGOelektro.png" alt="Logo" width="30px">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link text-light" href="Toko.html">Home</a></li>
                    <li class="nav-item"><a class="nav-link text-light" href="Products.html">Produk</a></li>
                    <li class="nav-item"><a class="nav-link text-light" href="#about">Tentang Kami</a></li>
                    <li class="nav-item"><a class="nav-link text-light" href="#contact">Hubungi Kami</a></li>
                    <li class="nav-item">
                        <a class="nav-link text-light" href="Cart.html">
                            <i class="fas fa-shopping-cart"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</header>

<!-- Add your content here -->
</body>
</html>
```

Here’s a detailed explanation of the key parts of the provided HTML and CSS to guide you step-by-step through the important lines:

---

### **HTML (Toko.html)**

#### **1. `<head>` Section**
This section contains metadata, links to external resources, and the title of the page.

- **`<link rel="stylesheet" type="text/css" href="tokoelektro.css">`**
  Links your custom CSS file (`tokoelektro.css`) to style the webpage.

- **Bootstrap CSS & FontAwesome**
  - **Bootstrap** is included via CDN to provide pre-designed components like the navbar, buttons, and grid system.
  - **FontAwesome** is added to use scalable vector icons (e.g., the shopping cart icon in the navbar).

---

#### **2. Navbar (Lines 14–32)**

The navbar allows users to navigate your website.

- **`<a class="navbar-brand" href="Toko.html">`**
  Links the logo to the homepage. This ensures the user can quickly return to the main page.

- **`<button class="navbar-toggler">`**
  Enables the collapsible navbar for smaller screens. It is part of Bootstrap's responsive features.

- **`<ul class="navbar-nav ms-auto mb-2 mb-lg-0">`**
  Creates a navigation list with links such as "Home," "Products," and "Contact Us."

---

#### **3. Featured Products (Lines 38–87)**

This section displays product cards dynamically with a grid layout.

- **`<div class="row row-cols-1 row-cols-md-2 row-cols-lg-4 g-4">`**
  Uses Bootstrap's grid system:
  - **`row-cols-1`**: One column per row on small screens.
  - **`row-cols-md-2`**: Two columns per row on medium screens.
  - **`row-cols-lg-4`**: Four columns per row on large screens.
  
- **Product Cards**
  - **`<div class="card product-card h-100">`**
    Uses Bootstrap’s card component for a clean design and ensures uniform height with `h-100`.

  - **`<img src="img/VR.png" class="card-img-top" alt="...">`**
    Adds a product image with a description for accessibility.

  - **`<form action="Cart.html" method="GET">`**
    Adds a "Buy Now" button. The form passes product details (e.g., name, price) to the cart page.

---

#### **4. About Us (Lines 117–127)**

This section introduces your store.

- **`<section id="about" class="container my-5 text-center">`**
  Adds an introduction about the store with a centered layout using Bootstrap utilities like `my-5` (margin) and `text-center`.

- **Logo Display**
  - **`<img src="img/LOGOelektro.png" width="120" alt="CoolGadgets Logo">`**
    Displays the store's logo prominently.

---

#### **5. Contact Form (Lines 133–147)**

A simple form for customer inquiries.

- **`<form>`**
  Contains input fields for name, email, and a message.

- **`<button type="submit" class="btn btn-warning">`**
  A submit button styled with Bootstrap's warning color class.

---

#### **6. Footer (Lines 149–176)**

The footer provides additional links and social media information.

- **Navigation and Useful Links**
  - Organized into columns using Bootstrap's grid system for clarity.

- **Social Media Icons**
  - **`<ul>`**: Links to platforms like Facebook, Twitter, Instagram, and YouTube.

---

### **CSS (tokoelektro.css)**

#### **1. Navbar**
- **`.navbar-collapse .navbar-nav .nav-item a:hover { color: #ff523b; }`**
  Changes the link color to orange when hovered over.

#### **2. Product Cards**
- **`.product-card img { height: 200px; object-fit: contain; width: 100%; }`**
  Ensures all product images have the same height and maintain aspect ratio.

- **Responsive Design**
  - **`@media (max-width: 768px)`**
    Adjusts image height to `150px` on tablets and smaller devices.

  - **`@media (max-width: 576px)`**
    Further reduces image height to `120px` for mobile devices.

#### **3. Card Titles**
- **`.card-title a { color: #333; text-decoration: none; }`**
  Ensures the product title links have a clean, readable appearance.

- **Hover Effect**
  - **`.card-title a:hover { color: #ff523b; }`**
    Changes the title link color to orange when hovered over.

---


---

### Step 2: Style the Website with CSS

The CSS file (`tokoelektro.css`) customizes the appearance of the website and ensures it looks good on different screen sizes.

```css
.navbar-collapse .navbar-nav .nav-item a:hover {
    color: #ff523b; 
}

.cart-item {
    margin-bottom: 1rem; 
}

.product-card {
    height: 100%;
}

.product-card img {
    height: 200px; 
    object-fit: contain;
    width: 100%;
}

@media (max-width: 768px) {
    .product-card img {
        height: 150px;
    }
}

@media (max-width: 576px) {
    .product-card img {
        height: 120px;
    }
    .product-card {
        margin-bottom: 20px;
    }
}

.card-title a {
    color: #333; 
    text-decoration: none; 
}

.card-title a:hover {
    color: #ff523b;
}
```

---

### Key Features

1. **Navbar**: Provides navigation between pages.
2. **Responsive Design**: Ensured via Bootstrap and custom CSS.
3. **Product Cards**: Display featured products with images, titles, and a "Buy Now" button.
4. **Footer**: Includes navigation links and social media handles.
5. **Contact Form**: Simple form to get user feedback.

---

### Future Steps You Can Do!!

1. **Add Functional JavaScript**: Use JavaScript for interactivity, such as cart functionality or product filtering.
2. **Enhance Backend**: Use a server-side language like Node.js to process orders and manage a database.
3. **Deploy the Website**: Host your site using platforms like Vercel, Netlify, or GitHub Pages. 

