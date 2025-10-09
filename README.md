# Ex.07 Restaurant Website
## Date:09/10/2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title> D Restaurant</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f8f8f8;
      color: #333;
    }
    header {
      background: #fff;
      text-align: center;
      padding: 20px;
    }
    header h1 {
      margin: 0;
      font-size: 28px;
    }
    nav {
      background: #333;
      text-align: center;
      padding: 10px 0;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 20px;
      font-weight: bold;
    }
    nav a:hover {
      color: #ffcc00;
    }
    .banner {
      background: url('Screenshot 2025-10-06 185705.png') no-repeat center/cover;
      color: white;
      padding: 60px 20px;
      text-align: center;
    }
    .banner h2 {
      font-size: 30px;
      margin-bottom: 10px;
    }
    .cards {
      display: flex;
      justify-content: space-around;
      margin: 20px;
      gap: 15px;
    }
    .card {
      background: #ffeedd;
      padding: 15px;
      border-radius: 10px;
      width: 30%;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    .card img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    .footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 20px;
    }
    .footer span {
      color: orange;
      font-weight: bold;
    }
    section {
      padding: 20px;
      display: none;
    }
    section.active {
      display: block;
    }
  </style>
  <script>
    function showPage(pageId) {
      let pages = document.querySelectorAll("section");
      pages.forEach(p => p.classList.remove("active"));
      document.getElementById(pageId).classList.add("active");
    }
  </script>
</head>
<body>

<header>
  <h1>spice&stories</h1>
</header>

<nav>
  <a href="#" onclick="showPage('home')">Home</a>
  <a href="#" onclick="showPage('menu')">Menu</a>
  <a href="#" onclick="showPage('admin')">Administration</a>
  <a href="#" onclick="showPage('contact')">Contact Us</a>
</nav>

<!-- Home Section -->
<section id="home" class="active">
  <div class="banner">
    <h2>30% Off This Weekend</h2>
    <p>Enjoy delicious meals with special discounts only at Little Lemon!</p>
  </div>

  <div class="cards">
    <div class="card">
      <h3>Our New Menu</h3>
      <img src="Screenshot 2025-10-06 185632.png" alt="Menu">
      <p>Check out our fresh and tasty new dishes for this season.</p>
    </div>
    <div class="card">
      <h3>Book a Table</h3>
      <img src="Screenshot 2025-10-06 185650.png" alt="Table">
      <p>Reserve your table easily and enjoy dining with us.</p>
    </div>
    <div class="card">
      <h3>Opening Hours</h3>
      <img src="Screenshot 2025-10-06 185720.png" alt="Hours">
      <p>Mon–Fri: 2pm - 10pm<br>Sat: 2pm - 11pm<br>Sun: 2pm - 9pm</p>
    </div>
  </div>
</section>

<!-- Menu Section -->
<section id="menu">
  <h2>Our Menu</h2>
  <ul>
    <li>Grilled Chicken Skewers</li>
    <li>Chicken friedrice</li>
    <li>parotta</li>
    <li>Pasta Alfredo</li>
    <li>Cheeseburger</li>
    <li>Fish Curry</li>
    <li>Chicken Biryani</li>
    <li>noodles</li>
    <li>Tandoori Paneer</li>
    <li>Garlic Naan</li>
    <li>Fruit Salad</li>
    <li>Chocolate Cake</li>
  </ul>
</section>

<!-- Administration Section -->
<section id="admin">
  <h2>Administration</h2>
  <ul>
    <li>thala dhoni – Manager</li>
    <li> devon conway– Chef</li>
    <li>sam curran Assistant Chef</li>
    <li>dhivya – Waitress</li>
    <li>Rajesh Waiter</li>
    <li>sushmitha – Cashier</li>
  </ul>
</section>

<!-- Contact Section -->
<section id="contact">
  <h2>Contact Us</h2>
  <p><b>Address:</b> 123 Main Street, City, India</p>
  <p><b>Phone:</b> +919790018465</p>
  <p><b>Email:</b> info@vishnupriya38.com</p>
</section>

<!-- Footer -->
<div class="footer">
  Designed and Developed by <span>vishnu,sushsmiths,mithra</span>
</div>

</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2025-10-06 191945.png>)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
