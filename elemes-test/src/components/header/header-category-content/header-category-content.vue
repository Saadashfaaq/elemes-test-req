<template>
  <div class="category-carousel ms-4">
    <div class="title-section">
      <h2 class="title">
        Browse Our Category <br />
        <span class="highlight">Receipt</span>
      </h2>
    </div>

    <div class="carousel-container">
      <div class="carousel-track" ref="carouselTrack">
        <div
          class="category-card"
          v-for="(category, index) in categories"
          :key="index"
          :style="{ backgroundColor: category.color }"
        >
          <font-awesome-icon :icon="category.icon" class="category-icon" />
          <h4>{{ category.name }}</h4>
          <p>{{ category.items }} Items</p>
        </div>
      </div>
    </div>
    <div class="d-flex flex-row-reverse gap-2 category-button">
      <button @click="nextSlide" class="nav-button">NEXT ➡</button>
      <button @click="prevSlide" class="nav-button">⬅ PREV</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import { library } from '@fortawesome/fontawesome-svg-core';
import { faPizzaSlice, faDrumstickBite, faFish, faBirthdayCake } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

library.add(faPizzaSlice, faDrumstickBite, faFish, faBirthdayCake);

export default {
  name: 'HeaderCategorySection',
  components: {
    FontAwesomeIcon
  },
  setup() {
    const carouselTrack = ref(null);
    const scrollAmount = 300;

    const nextSlide = () => {
      if (carouselTrack.value) {
        carouselTrack.value.scrollLeft += scrollAmount;
      }
    };

    const prevSlide = () => {
      if (carouselTrack.value) {
        carouselTrack.value.scrollLeft -= scrollAmount;
      }
    };

    return { carouselTrack, nextSlide, prevSlide };
  },
  data() {
    return {
      categories: [
        { name: "Cupcake", items: 22, icon: "fa-birthday-cake", color: "#e9f9e5" },
        { name: "Pizza", items: 25, icon: "fa-pizza-slice", color: "#e0ecf9" },
        { name: "Kebab", items: 12, icon: "fa-drumstick-bite", color: "#f9e0e0" },
        { name: "Salmon", items: 22, icon: "fa-fish", color: "#f3d9e0" },
        { name: "Cupcake", items: 22, icon: "fa-birthday-cake", color: "#e9f9e5" },
        { name: "Pizza", items: 25, icon: "fa-pizza-slice", color: "#e0ecf9" },
        { name: "Kebab", items: 12, icon: "fa-drumstick-bite", color: "#f9e0e0" },
        { name: "Salmon", items: 22, icon: "fa-fish", color: "#f3d9e0" },
        { name: "Cupcake", items: 22, icon: "fa-birthday-cake", color: "#e9f9e5" },
        { name: "Pizza", items: 25, icon: "fa-pizza-slice", color: "#e0ecf9" },
        { name: "Kebab", items: 12, icon: "fa-drumstick-bite", color: "#f9e0e0" },
        { name: "Salmon", items: 22, icon: "fa-fish", color: "#f3d9e0" },
        { name: "Cupcake", items: 22, icon: "fa-birthday-cake", color: "#e9f9e5" },
        { name: "Pizza", items: 25, icon: "fa-pizza-slice", color: "#e0ecf9" },
        { name: "Kebab", items: 12, icon: "fa-drumstick-bite", color: "#f9e0e0" },
        { name: "Salmon", items: 22, icon: "fa-fish", color: "#f3d9e0" },
        { name: "Cupcake", items: 22, icon: "fa-birthday-cake", color: "#e9f9e5" },
        { name: "Pizza", items: 25, icon: "fa-pizza-slice", color: "#e0ecf9" },
        { name: "Kebab", items: 12, icon: "fa-drumstick-bite", color: "#f9e0e0" },
        { name: "Salmon", items: 22, icon: "fa-fish", color: "#f3d9e0" }
      ]
    };
  }
};
</script>

<style scoped>
.category-carousel {
  text-align: center;
  padding: 20px;
}

.title {
  font-size: 24px;
  font-weight: bold;
}

.title-section {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-left: 80px;
}

.highlight {
  color: #7db442;
}

.carousel-container {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  margin-top: 20px;
}

.carousel-track {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  gap: 15px;
  padding: 10px;
  width: 100%;
  white-space: nowrap;
}

.carousel-track::-webkit-scrollbar {
  display: none;
}

.category-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  width: 150px;
  height: 150px;
  text-align: center;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  flex-shrink: 0;
  padding-top: 15px;
}

.category-icon {
  font-size: 32px;
  margin-bottom: 10px;
}

.nav-button {
  background-color: #7db442;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 20px;
  cursor: pointer;
  font-size: 14px;
}

.nav-button:hover {
  background-color: #6a9c38;
}

@media (max-width: 768px) {
  .carousel-track {
    width: 100%;
  }
  .category-card {
    width: 120px;
    height: 120px;
  }
  .nav-button {
    display: none;
  }
}
</style>