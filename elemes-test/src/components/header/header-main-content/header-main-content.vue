<template>
  <div class="header-container ms-4">
    <!-- Left Section -->
    <div class="header-text">
      <h1 class="header-title">
        Good Food Us <br> Good Mood
      </h1>
      <p class="header-description">
        I would think that conserving our natural resources should be a conservative position:
        Not to waste food, and not to throw away a lot of the food that we buy.
      </p>
      <div class="header-buttons">
        <button class="btn btn-success header-btn">Daftar Sekarang</button>
        <button class="btn btn-light header-btn header-btn-light">About Us</button>
      </div>
    </div>

    <!-- Right Section -->
    <div class="header-image-container">
      <div class="header-image-wrapper">
        <img src="https://img.hellofresh.com/w_3840,q_auto,f_auto,c_fill,fl_lossy/hellofresh_s3/image/601046e74a46755e44641fc2-e2968f9f.jpg" 
             alt="Food" 
             class="header-image">
        
        <!-- Floating Card -->
        <div class="floating-card">
          <img src="https://img.hellofresh.com/w_3840,q_auto,f_auto,c_fill,fl_lossy/hellofresh_s3/image/601046e74a46755e44641fc2-e2968f9f.jpg" 
               alt="Green Salad Tomato" 
               class="floating-card-image">
          <div class="floating-card-content">
            <h6 class="floating-card-title">Green Salad Tomato</h6>
            <p class="floating-card-subtitle">Tomato</p>
            <div class="floating-card-rating">★★★★★</div>
          </div>
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


<style scoped>
.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2rem;
  background-color: white;
  flex-direction: column;
}

@media (min-width: 768px) {
  .header-container {
    flex-direction: row;
  }
}

.header-text {
  text-align: center;
  width: 100%;
}

@media (min-width: 768px) {
  .header-text {
    text-align: left;
    width: 50%;
  }
}

.header-title {
  font-size: 2.5rem;
  font-weight: bold;
  color: #28a745;
  line-height: 1.3;
}

.header-description {
  color: #6c757d;
  margin-top: 1rem;
}

.header-buttons {
  margin-top: 1.5rem;
  display: flex;
  justify-content: center;
}

@media (min-width: 768px) {
  .header-buttons {
    justify-content: flex-start;
  }
}

.header-btn {
  padding: 0.5rem 1.5rem;
  border-radius: 50px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  margin-right: 0.5rem;
}

.header-btn-light {
  border: 1px solid #ddd;
}

.header-image-container {
  display: flex;
  justify-content: center;
  width: 100%;
  margin-top: 1rem;
}

@media (min-width: 768px) {
  .header-image-container {
    width: 50%;
    margin-top: 0;
  }
}

.header-image-wrapper {
  position: relative;
  width: 350px;
  height: 350px;
}

.header-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
}

.floating-card {
  position: absolute;
  bottom: 10px;
  right: 10px;
  background-color: white;
  padding: 1rem;
  border-radius: 15px;
  display: flex;
  align-items: center;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  width: 200px;
}

.floating-card-image {
  width: 50px;
  height: 50px;
  object-fit: cover;
  border-radius: 50%;
}

.floating-card-content {
  margin-left: 0.75rem;
}

.floating-card-title {
  font-weight: bold;
  margin-bottom: 0;
}

.floating-card-subtitle {
  color: #6c757d;
  font-size: 0.85rem;
  margin-bottom: 0.25rem;
}

.floating-card-rating {
  color: #ffc107;
  font-size: 0.85rem;
}

</style>