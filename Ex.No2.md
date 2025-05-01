# Ex02 Commercial Website

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
### index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CommercialX | Innovative Solutions</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <!-- Navigation Bar -->
  <header>
    <div class="nav-container">
      <h1 class="logo">Commercial<span>X</span></h1>
      <nav>
        <a href="#home">Home</a>
        <a href="#products">Products</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a href="#account">Account</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h2>Innovate Your Business</h2>
      <p>Experience the future of commerce with our cutting-edge solutions.</p>
      <a href="#products" class="btn">Explore Products</a>
    </div>
    <div class="hero-image">
      <img src="hero-image.png" alt="Innovative Solutions" class="floating" />
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="products">
    <h2>Our Products</h2>
    <div class="product-grid">
      <div class="product-card">
        <img src="product1.png" alt="Product 1" class="product-image floating" />
        <h3>Product One</h3>
        <p>Revolutionary features for modern businesses.</p>
      </div>
      <div class="product-card">
        <img src="product2.png" alt="Product 2" class="product-image floating" />
        <h3>Product Two</h3>
        <p>Streamline your operations with ease.</p>
      </div>
      <div class="product-card">
        <img src="product3.png" alt="Product 3" class="product-image floating" />
        <h3>Product Three</h3>
        <p>Advanced analytics for informed decisions.</p>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="about">
    <h2>About Us</h2>
    <p>At CommercialX, we are dedicated to delivering innovative solutions that empower businesses to thrive in the digital era.</p>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <p>Email: contact@commercialx.com</p>
    <p>Phone: +91-9876543210</p>
  </section>

  <!-- Account Section -->
  <section id="account" class="account">
    <h2>User Account</h2>
    <p>Access your personalized dashboard and manage your preferences.</p>
    <a href="#" class="btn-outline">Sign In</a>
  </section>

  <!-- Footer -->
  <footer>
    <div class="social-icons">
      <a href="#"><img src="images/facebook.svg" alt="Facebook"></a>
      <a href="#"><img src="images/twitter.svg" alt="Twitter"></a>
      <a href="#"><img src="images/linkedin.svg" alt="LinkedIn"></a>
    </div>
    <p>&copy; 2025 CommercialX. All rights reserved.</p>
  </footer>
</body>
</html>

```
### index.css
```
/* === GLOBAL STYLES === */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
    color: #333;
    line-height: 1.6;
  }
  a {
    text-decoration: none;
    color: #333;
    transition: color 0.3s ease;
  }
  a:hover {
    color: #0077ff;
  }
  
  /* === NAVIGATION === */
  .nav-container {
    background: #ffffffcc;
    backdrop-filter: blur(8px);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    box-shadow: 0 4px 8px rgba(0,0,0,0.05);
  }
  .logo {
    font-size: 1.8rem;
    font-weight: bold;
  }
  .logo span {
    color: #0077ff;
  }
  nav a {
    margin-left: 1.5rem;
    font-weight: 500;
  }
  
  /* === HERO SECTION === */
  .hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3rem 2rem;
  }
  .hero-content {
    flex: 1;
  }
  .hero-content h2 {
    font-size: 3rem;
    color: #222;
  }
  .hero-content p {
    margin: 1rem 0;
  }
  .btn {
    background: #54bcdc;
    color: white;
    padding: 0.8rem 1.5rem;
    border-radius: 30px;
    display: inline-block;
    margin-top: 1rem;
  }
  .hero-image img {
    width: 300px;
    animation: float 3s ease-in-out infinite;
  }
  
  /* === FLOATING ANIMATION === */
  @keyframes float {
    0%, 100% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-20px);
    }
  }
  
  /* === PRODUCTS SECTION === */
  .products {
    padding: 3rem 2rem;
    text-align: center;
  }
  .product-grid {
    display: flex;
    gap: 2rem;
    justify-content: center;
    flex-wrap: wrap;
  }
  .product-card {
    background: #fff;
    padding: 2rem;
    border-radius: 15px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    width: 250px;
    transition: transform 0.3s ease;
  }
  .product-card:hover {
    transform: translateY(-10px);
  }
  .product-image {
    width: 100%;
    height: auto;
    margin-bottom: 1rem;
    animation: float 4s ease-in-out infinite;
  }
  
  /* === ABOUT, CONTACT, ACCOUNT === */
  section {
    padding: 2rem 2rem;
  }
  .about, .contact, .account {
    background: #f8f8f8;
    margin: 2rem 0;
    border-radius: 15px;
  }
  
  /* === USER IMAGE ROUND FRAME === */
  .round-profile {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid #0077ff;
    margin: 1rem auto;
    display: block;
  }
  
  /* === FOOTER === */
  footer {
    background: #222;
    color: white;
    padding: 1rem;
    text-align: center;
  }
  .social-icons img {
    width: 30px;
    margin: 0 10px;
    transition: transform 0.3s;
  }
  .social-icons img:hover {
    transform: scale(1.2);
  }
  
```

## OUTPUT
![image](https://github.com/user-attachments/assets/4cb4e3e6-584d-415c-b1a5-ccfe3a2b9254)


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
