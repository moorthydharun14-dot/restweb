# Ex.07 Restaurant Website
## Date:16/10/2025

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
base.html
{% load static %}
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>{% block title %}Spice Delight{% endblock %}</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  margin: 0; padding: 0;
}

header {
  background-color: #c0392b;
  padding: 10px;
  color: white;
}

nav ul {
  list-style: none;
  text-align: center;
  padding: 0;
}

nav ul li {
  display: inline-block;
  margin: 0 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

.banner {
  width: 100%;
  height: 300px;
  object-fit: cover;
}

.intro {
  padding: 40px;
  text-align: center;
}

.menu-grid, .team-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  padding: 20px;
}

.menu-grid .item img, .team-grid .member img {
  width: 100%;
  border-radius: 10px;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
}

</style>

</head>
<body>
  <header>
    <img src="{% static 'images/banner.png'%}" alt="Banner" class="banner">
    <nav>
      <ul>
        <li><a href="{% url 'home' %}">Home</a></li>
        <li><a href="{% url 'menu' %}">Menu</a></li>
        <li><a href="{% url 'administration' %}">Administration</a></li>
        <li><a href="{% url 'contact' %}">Contact Us</a></li>
      </ul>
    </nav>
  </header>

  <main>
    {% block content %}{% endblock %}
  </main>

  <footer>
    <p>Designed by Akash A © 2025</p>
  </footer>
</body>
</html>
home.html
{% extends 'base.html' %}
{% block title %}Home — Spice Delight{% endblock %}
{% block content %}
<section class="intro">
  <h1>Welcome to Spice Delight</h1>
  <p>Serving traditional flavors with a modern twist. Join us for an unforgettable experience.</p>
</section>
{% endblock %}
menu.html
{% extends 'base.html' %}
{% load static %}
{% block title %}Menu — Spice Delight{% endblock %}
{% block content %}
<section class="menu">
  <h2>Our Menu</h2>
  <div class="menu-grid">
    {% for food in foods %}
      <div class="item">
        <img src="{% static 'images/'|add:food.image %}" alt="{{ food.name }}">
        <p>{{ food.name }}</p>
      </div>
    {% endfor %}
  </div>
</section>
{% endblock %}
admin.html
{% extends 'base.html' %}
{% block title %}Administration — Spice Delight{% endblock %}
{% block content %}
<section class="team">
  <h2>Our Team</h2>
  <div class="team-grid">
    {% for member in team %}
      <div class="member">
        <img src="{% static 'images/'|add:member.image %}" alt="{{ member.name }}">
        <p>{{ member.name }} – {{ member.role }}</p>
      </div>
    {% endfor %}
  </div>
</section>
{% endblock %}
contact.html
% extends 'base.html' %}
{% block title %}Contact Us — Spice Delight{% endblock %}
{% block content %}
<section class="contact">
  <h2>Contact Us</h2>
  <p>📍 Address: {{ contact.address }}</p>
  <p>📞 Phone: {{ contact.phone }}</p>
  <p>✉ Email: {{ contact.email }}</p>
</section>
{% endblock %}
views.py
from django.shortcuts import render

def home_view(request):
    return render(request, 'home.html')

def menu_view(request):
    # example food list
    foods = [
        {'name': 'Biryani', 'image': 'images/biryani.png'},
        {'name': 'Pizza', 'image': 'images/pizza.png'},
        {'name': 'Pasta', 'image': 'images/Noddles.png'},
        # add up to 12 ...
    ]
    return render(request, 'menu.html', {'foods': foods})

def admin_view(request):
    # team members list
    team = [
        {'name': 'Raj', 'role': 'Head Chef', 'image': 'team/raj.jpg'},
        {'name': 'Anjali', 'role': 'Manager', 'image': 'team/anjali.jpg'},
        # add 4 more ...
    ]
    return render(request, 'administration.html', {'team': team})

def contact_view(request):
    contact_info = {
        'address': '123 Spice Street, Chennai City',
        'phone': '+91-9876543210',
        'email': 'contact@spicedelight.com',
    }
    return render(request, 'contact.html', {'contact': contact_info})
    urls.py
    from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('core.urls')),
]

```


## OUTPUT
<img width="1920" height="1080" alt="Screenshot 2025-10-16 114350" src="https://github.com/user-attachments/assets/53e8fe6d-dd61-4b81-b043-c3848a024d5b" />
<img width="1920" height="1080" alt="Screenshot 2025-10-16 114402" src="https://github.com/user-attachments/assets/a69905d4-5992-4354-95a6-84737f9df1d4" />


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
