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
    path('', views.home, name='home'),
    path('medicines/', views.medicines, name='medicines'),
    path('wellness/', views.wellness, name='wellness'),
    path('contact/', views.contact, name='contact'),
]
views.py
from django.shortcuts import render

def home(request):
    return render(request, 'index.html')

def medicines(request):
    return render(request, 'medicines.html')

def wellness(request):
    return render(request, 'wellness.html')

def contact(request):
    return render(request, 'contact.html')

index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>HealthPlus Pharmacy - Home</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">HealthPlus</a>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link active" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="medicines.html">Medicines</a></li>
          <li class="nav-item"><a class="nav-link" href="wellness.html">Wellness</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <section class="bg-light text-center py-5">
    <div class="container">
      <h1 class="display-4 text-primary">Your Trusted Online Pharmacy</h1>
      <p class="lead">Order medicines, health products, and wellness essentials delivered to your door.</p>
      <a href="medicines.html" class="btn btn-primary btn-lg">Shop Medicines</a>
    </div>
  </section>

  <section class="py-5">
    <div class="container">
      <h2 class="text-center mb-4">Popular Categories</h2>
      <div class="row g-4">
        <div class="col-md-3"><div class="card"><div class="card-body text-center">Pain Relief</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body text-center">Vitamins</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body text-center">Skin Care</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body text-center">Baby Care</div></div></div>
      </div>
    </div>
  </section>

  <footer class="bg-primary text-white text-center py-3">
    <p>&copy; 2025 HealthPlus Pharmacy</p>
  </footer>
</body>
</html>

medicines.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Medicines - HealthPlus Pharmacy</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">HealthPlus</a>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link active" href="medicines.html">Medicines</a></li>
          <li class="nav-item"><a class="nav-link" href="wellness.html">Wellness</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <section class="py-5">
    <div class="container">
      <h2 class="mb-4">Medicines</h2>
      <div class="row g-4">
        <div class="col-md-3"><div class="card"><div class="card-body">Paracetamol</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body">Ibuprofen</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body">Antibiotics</div></div></div>
        <div class="col-md-3"><div class="card"><div class="card-body">Cough Syrup</div></div></div>
      </div>
    </div>
  </section>

  <footer class="bg-primary text-white text-center py-3">
    <p>&copy; 2025 HealthPlus Pharmacy</p>
  </footer>
</body>
</html>

wellness.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Wellness - HealthPlus Pharmacy</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">HealthPlus</a>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="medicines.html">Medicines</a></li>
          <li class="nav-item"><a class="nav-link active" href="wellness.html">Wellness</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <section class="py-5">
    <div class="container">
      <h2 class="mb-4">Wellness & Health Tips</h2>
      <div class="row g-4">
        <div class="col-md-6"><div class="card"><div class="card-body">💪 Exercise regularly</div></div></div>
        <div class="col-md-6"><div class="card"><div class="card-body">🥗 Eat balanced meals</div></div></div>
        <div class="col-md-6"><div class="card"><div class="card-body">💧 Stay hydrated</div></div></div>
        <div class="col-md-6"><div class="card"><div class="card-body">😴 Get enough sleep</div></div></div>
      </div>
    </div>
  </section>

  <footer class="bg-primary text-white text-center py-3">
    <p>&copy; 2025 HealthPlus Pharmacy</p>
  </footer>
</body>
</html>

contact.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Contact - HealthPlus Pharmacy</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">HealthPlus</a>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="medicines.html">Medicines</a></li>
          <li class="nav-item"><a class="nav-link" href="wellness.html">Wellness</a></li>
          <li class="nav-item"><a class="nav-link active" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>
</body>
```
# OUTPUT:
<img width="1919" height="973" alt="Screenshot 2025-12-27 071506" src="https://github.com/user-attachments/assets/03da1f08-29d8-49e4-9563-7c4d9ed7690f" />
<img width="1920" height="1080" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/a3b6b5a2-2053-4fef-aa7f-552df55af5fb" />
<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/5a298ed9-2305-4279-a791-d11cba59dac5" />


# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
