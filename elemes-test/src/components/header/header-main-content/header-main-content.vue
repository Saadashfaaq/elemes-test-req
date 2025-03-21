<template>
  <div class="d-flex align-items-center justify-content-between p-5 bg-white position-relative">
    <!-- Left Section -->
    <div class="w-50">
      <h1 class="display-4 fw-bold text-success lh-base">
        Good Food Us <br> Good Mood
      </h1>
      <p class="text-secondary mt-3">
        I would think that conserving our natural resources should be a conservative position:
        Not to waste food, and not to throw away a lot of the food that we buy.
      </p>
      <div class="mt-4">
        <button class="btn btn-success me-3 px-4 py-2 rounded-pill shadow">
          Daftar Sekarang
        </button>
        <button class="btn btn-light px-4 py-2 rounded-pill shadow border">
          About Us
        </button>
      </div>
    </div>

    <!-- Right Section -->
    <div class="w-50 position-relative text-center">
      <img src="/path-to-your-image.jpg" alt="Food" class="img-fluid rounded-circle shadow-lg" style="width: 350px; height: 350px; object-fit: cover;">
      
      <!-- Floating Card -->
      <div class="position-absolute bg-white p-3 rounded shadow-sm d-flex align-items-center" style="bottom: 20px; left: 50px; width: 200px;">
        <img src="/path-to-your-small-image.jpg" alt="Green Salad Tomato" class="rounded-circle" style="width: 50px; height: 50px; object-fit: cover;">
        <div class="ms-3">
          <h6 class="fw-bold mb-0">Green Salad Tomato</h6>
          <p class="text-muted mb-1 small">Tomato</p>
          <div class="text-warning small">★★★★★</div>
        </div>
      </div>
    </div>
  </div>
</template>



<script>
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';

export default {
  name: 'HeaderMainSection',
  props: {
    msg: String
  }
}
</script>
