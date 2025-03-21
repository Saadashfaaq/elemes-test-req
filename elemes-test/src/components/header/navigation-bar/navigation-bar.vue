<template>
  <nav class="navbar navbar-expand-lg navbar-light fixed-top" style="background: rgba(255, 255, 255, 0.9);">
    <div class="container-fluid px-3 px-md-5 d-flex justify-content-between align-items-center">
      <!-- Logo -->
      <a class="navbar-brand d-flex align-items-center" href="#">
        <div class="ms-2 text-start">
          <h2 class="text-primary">elemes.<span class="text-dark">id</span></h2>
          <p class="fs-6 text-muted mb-0 d-none d-md-block">Product and Tech Agency Company</p>
        </div>
      </a>

      <!-- Navbar Links (Hidden on Mobile) -->
      <div class="collapse navbar-collapse justify-content-center d-none d-lg-flex" id="navbarNav">
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
        <a href="#" class="text-dark text-decoration-none d-none d-lg-block">Masuk</a>
        <button class="btn btn-success rounded-pill px-4">Daftar Sekarang</button>
      </div>
    </div>
  </nav>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';

export default {
  name: 'navigationSection'
}
</script>

<style scoped>
/* Menyembunyikan elemen yang tidak perlu di tampilan mobile */
@media (max-width: 991px) {
  #navbarNav, .nav-item, .text-muted { 
    display: none !important; 
  }
}
</style>