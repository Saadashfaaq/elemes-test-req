<template>
  <nav class="navbar navbar-expand-lg navbar-light fixed-top" style="background: rgba(255, 255, 255, 0.9);">
    <div class="container-fluid px-5">
      <!-- Logo -->
      <a class="navbar-brand d-flex align-items-center" href="#">
        <img src="/path-to-logo.png" alt="Logo" style="height: 40px;">
        <div class="ms-2">
          <strong class="text-primary">elemes.<span class="text-dark">id</span></strong>
          <p class="small text-muted mb-0">Product and Tech Agency Company</p>
        </div>
      </a>

      <!-- Toggle Button -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Navbar Links -->
      <div class="collapse navbar-collapse justify-content-center" id="navbarNav">
        <ul class="navbar-nav gap-3">
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">About</a>
          </li>
          <li class="nav-item position-relative">
            <a class="nav-link text-dark" href="#">Promotions</a>
            <span class="position-absolute top-0 start-100 translate-middle badge bg-danger small">HOT</span>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">Blogs</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">Contact Us</a>
          </li>
        </ul>
      </div>

      <!-- Buttons -->
      <div class="d-flex align-items-center gap-3">
        <a href="#" class="text-dark text-decoration-none">Masuk</a>
        <button class="btn btn-success rounded-pill px-4">Daftar Sekarang</button>
      </div>
    </div>
  </nav>
</template>


<script>
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';

export default {
  name: 'navigationSection',
  props: {
    msg: String
  }
}
</script>
