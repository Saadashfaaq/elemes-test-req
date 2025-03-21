<template>
  <div class="container mt-5">
    <h2 class="fw-bold">Browser Our Trending</h2>
    <h3 class="text-success">Receipt</h3>

    <div class="row row-cols-1 row-cols-md-4 g-4">
      <div class="col" v-for="(item, index) in recipes" :key="index">
        <div class="card p-3 border-0 shadow-sm" :style="{ backgroundColor: item.bgColor }">
          <img :src="item.image" class="card-img-top rounded" alt="Food Image">
          <div class="card-body">
            <h5 class="card-title fw-bold">{{ item.title }}</h5>
            <p class="text-muted mb-1">{{ item.category }}</p>
            <div class="text-warning">
              <span v-for="star in 5" :key="star">
                <i class="bi" :class="star <= item.rating ? 'bi-star-fill' : 'bi-star'" ></i>
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="text-center mt-4">
      <button class="btn btn-success rounded-pill px-4">ALL Receipt</button>
    </div>
  </div>
</template>

<script>
export default {
    name: 'contentSection',
  props: {
    msg: String
  },
  data() {
    return {
      recipes: [
        { title: 'Pizza Paperoni', category: 'Pizza', rating: 4, image: 'https://via.placeholder.com/150', bgColor: '#E3F2FD' },
        { title: 'Pizza Meat', category: 'Pizza', rating: 3, image: 'https://via.placeholder.com/150', bgColor: '#E0F7FA' },
        { title: 'Doner Kebab', category: 'Kebab', rating: 5, image: 'https://via.placeholder.com/150', bgColor: '#E8F5E9' },
        { title: 'Salmon Roll', category: 'Salmon', rating: 4, image: 'https://via.placeholder.com/150', bgColor: '#FCE4EC' },
        { title: 'Cupcake Choco', category: 'Cupcake', rating: 4, image: 'https://via.placeholder.com/150', bgColor: '#F1F8E9' },
        { title: 'Doughnut Milk', category: 'Doughnut', rating: 5, image: 'https://via.placeholder.com/150', bgColor: '#FFF9C4' },
        { title: 'Doughnut Unicorn', category: 'Doughnut', rating: 4, image: 'https://via.placeholder.com/150', bgColor: '#F3E5F5' },
        { title: 'Kathi Kebab', category: 'Kebab', rating: 4, image: 'https://via.placeholder.com/150', bgColor: '#E3F2FD' },
      ]
    };
  }
};
</script>

<style>
.card {
  border-radius: 12px;
}
.card img {
  height: 120px;
  object-fit: cover;
}
.bi-star-fill {
  color: #ffc107;
}
.bi-star {
  color: #e0e0e0;
}
</style>


<!-- <script>


export default {
  name: 'contentSection',
  props: {
    msg: String
  }
}
</script> -->
