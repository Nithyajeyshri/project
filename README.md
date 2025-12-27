# Project Responsive Web Design using Bootstrap
# Date:23-12-2025
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
urls.py

from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
views.py

from django.shortcuts import render

def index(request):
    return render(request, 'index.html')

index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Nithya - Online E-Pharmacy store</title>
  
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background-color: #f8f9fa;
    }
    header {
      background: linear-gradient(135deg, #9c28a7, #502c9f);
      padding: 50px 0;
      color: white;
    }
    .navbar {
      background-color: #191987;
    }
    .navbar-nav .nav-link {
      color: white !important;
      font-weight: 500;
    }
    .hero {
      background: linear-gradient(135deg, #ff6f61, #d63384, #6f42c1);
      padding: 120px 0;
      color: #fff;
      text-align: center;
}
      
    .card img {
      height: 200px;
      object-fit: contain;
      padding: 10px;
    }
    .card {
      border: none;
      transition: transform 0.3s;
    }
    .card:hover {
      transform: scale(1.05);
    }
    footer {
      background-color: #343a40;
      padding: 20px;
      color: white;
      margin-top: 50px;
    }
  </style>
</head>

<body>

  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="container">
      <a class="navbar-brand fw-bold" href="#">Nithya Pharmacy</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#products">Products</a></li>
          <li class="nav-item"><a class="nav-link" href="#offers">Offers</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact Us</a></li>
        </ul>
      </div>
    </div>
  </nav>
 
  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <h1 class="display-4 fw-bold">Nithya's Pharmacy</h1>
      <p class="lead">Care for your health, delivered with trust 💊. Because wellness starts here — shop medicines, essentials, and healthcare products online with ease. Fast delivery, genuine products, and your well‑being always come first.</p>

      <a href="#products" class="btn btn-light btn-lg mt-3">Shop Now</a>
    </div>
  </section>

  <!-- Men’s Fashion Products -->
  <section class="container my-5" id="products">
    <h2 class="text-center mb-4 fw-bold">Medicines</h2>
    <div class="row g-4">
      <!-- Product 1 -->
      <div class="col-md-3 col-sm-6">
        <div class="card shadow-sm text-center">
          <img src="{% static 'images/img1.webp' %}" alt="paracetamol">
          <div class="card-body">
            <h5 class="card-title">Paracetamol</h5>
            <p class="card-text text-success fw-bold">₹40</p>
            <button class="btn btn-success btn-sm">Add to Cart</button>
          </div>
        </div>
      </div>
      <!-- Product 2 -->
      <div class="col-md-3 col-sm-6">
        <div class="card shadow-sm text-center">
          <img src="{% static 'images/img3.webp' %}" alt="cough syrup">
          <div class="card-body">
            <h5 class="card-title">Cough syrup</h5>
            <p class="card-text text-success fw-bold">₹350</p>
            <button class="btn btn-success btn-sm">Add to Cart</button>
          </div>
        </div>
      </div>
      <!-- Product 3 -->
      <div class="col-md-3 col-sm-6">
        <div class="card shadow-sm text-center">
          <img src="{% static 'images/img2.avif' %}" alt="Vitamin-C">
          <div class="card-body">
            <h5 class="card-title">Vitamin-C</h5>
            <p class="card-text text-success fw-bold">₹150</p>
            <button class="btn btn-success btn-sm">Add to Cart</button>
          </div>
        </div>
      </div>
      <!-- Product 4 -->
      <div class="col-md-3 col-sm-6">
        <div class="card shadow-sm text-center">
          <img src="{% static 'images/img4.webp' %}" alt="Sanitizer">
          <div class="card-body">
            <h5 class="card-title">Sanitizer</h5>
            <p class="card-text text-success fw-bold">₹200</p>
            <button class="btn btn-success btn-sm">Add to Cart</button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Offers Section -->
  <section class="bg-light py-5" id="offers">
    <div class="container text-center">
      <h2>Exclusive Offers</h2>
      <p class="lead">Up to 40% off on your first order! Use code <strong>NITHYA40</strong></p>
      <a href="#products" class="btn btn-success">Shop Offers</a>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="container my-5" id="contact">
    <h2 class="text-center mb-4">Contact Us</h2>
    <div class="row justify-content-center">
      <div class="col-md-6">
        <form>
          <div class="mb-3">
            <label class="form-label">Name</label>
            <input type="text" class="form-control" placeholder="Your Name">
          </div>
          <div class="mb-3">
            <label class="form-label">Email</label>
            <input type="email" class="form-control" placeholder="Your Email">
          </div>
          <div class="mb-3">
            <label class="form-label">Message</label>
            <textarea class="form-control" rows="4" placeholder="Your Message"></textarea>
          </div>
          <button class="btn btn-success w-100">Submit</button>
        </form>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="text-center">
    <p>Designed by Nithya</p>
  </footer>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
# OUTPUT:
<img width="1920" height="1080" alt="Screenshot (69)" src="https://github.com/user-attachments/assets/042a695b-ef78-44bb-9d28-4fda6a3f1bfa" />
<img width="1920" height="1080" alt="Screenshot (70)" src="https://github.com/user-attachments/assets/ab37d8ff-031a-4ad5-bbf5-5e7fa4c695e7" />
<img width="1920" height="1080" alt="Screenshot (71)" src="https://github.com/user-attachments/assets/4ac47004-416b-4812-b946-2d3095538da7" />
# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
