<template>
  <div class="category-carousel">
    <h2 class="title">
      Browser Our Category <br />
      <span class="highlight">Receipt</span>
    </h2>

    <!-- Wrapper untuk slider -->
    <div class="carousel-container">
      <button @click="prevSlide" class="nav-button prev">⬅ PREV</button>
      
      <div class="carousel-track" ref="carouselTrack">
        <div
          class="category-card"
          v-for="(category, index) in categories"
          :key="index"
          :style="{ backgroundColor: category.color }"
        >
          <img :src="category.image" alt="category icon" class="category-icon" />
          <h3>{{ category.name }}</h3>
          <p>{{ category.items }} Items</p>
        </div>
      </div>

      <button @click="nextSlide" class="nav-button next">NEXT ➡</button>
    </div>
  </div>
</template>

<script>
import { onMounted } from 'vue';
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';

export default {
  name: 'HeaderCategorySection',
  setup() {
    onMounted(() => {
      import('bootstrap').then(({ Carousel }) => {
        new Carousel(document.querySelector('#carouselExample'));
      });
    });
  },
    data() {
    return {
      scrollAmount: 250, // Seberapa jauh geser per klik
      categories: [
        { name: "Cupcake", items: 22, image: "/assets/cupcake.png", color: "#e9f9e5" },
        { name: "Pizza", items: 25, image: "/assets/pizza.png", color: "#e0ecf9" },
        { name: "Kebab", items: 12, image: "/assets/kebab.png", color: "#f9e0e0" },
        { name: "Salmon", items: 22, image: "/assets/salmon.png", color: "#f3d9e0" },
        { name: "Doughnut", items: 11, image: "/assets/doughnut.png", color: "#eef9e5" },
        { name: "Kebab", items: 12, image: "/assets/kebab.png", color: "#f9e0e0" },
        { name: "Salmon", items: 22, image: "/assets/salmon.png", color: "#f3d9e0" },
        { name: "Doughnut", items: 11, image: "/assets/doughnut.png", color: "#eef9e5" },
        { name: "Kebab", items: 12, image: "/assets/kebab.png", color: "#f9e0e0" },
        { name: "Salmon", items: 22, image: "/assets/salmon.png", color: "#f3d9e0" },
        { name: "Doughnut", items: 11, image: "/assets/doughnut.png", color: "#eef9e5" },
        { name: "Kebab", items: 12, image: "/assets/kebab.png", color: "#f9e0e0" },
        { name: "Salmon", items: 22, image: "/assets/salmon.png", color: "#f3d9e0" },
        { name: "Doughnut", items: 11, image: "/assets/doughnut.png", color: "#eef9e5" }
      ],
    };
  },
  methods: {
    nextSlide() {
      this.$refs.carouselTrack.scrollLeft += this.scrollAmount;
    },
    prevSlide() {
      this.$refs.carouselTrack.scrollLeft -= this.scrollAmount;
    },
  },
};
</script>


<style scoped>
/* Gaya dasar */
.category-carousel {
  text-align: center;
  padding: 20px;
}

.title {
  font-size: 24px;
  font-weight: bold;
}

.highlight {
  color: #7db442;
}

/* Container untuk carousel */
.carousel-container {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  margin-top: 20px;
}

/* Track tempat kategori berada */
.carousel-track {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  gap: 15px;
  padding: 10px;
  width: 80%;
  white-space: nowrap;
}

/* Menyembunyikan scrollbar */
.carousel-track::-webkit-scrollbar {
  display: none;
}

/* Kartu kategori */
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
}

.category-icon {
  width: 50px;
  height: 50px;
  margin-bottom: 10px;
}

/* Tombol navigasi */
.nav-button {
  background-color: #7db442;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 20px;
  cursor: pointer;
  font-size: 14px;
  position: absolute;
}

.prev {
  left: 5px;
}

.next {
  right: 5px;
}

.nav-button:hover {
  background-color: #6a9c38;
}

/* Responsif */
@media (max-width: 768px) {
  .carousel-track {
    width: 100%;
  }
  .category-card {
    width: 120px;
    height: 120px;
  }
}
</style>