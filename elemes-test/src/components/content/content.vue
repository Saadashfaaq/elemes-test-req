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
            <div class="floating-card-rating">★★★★★</div>
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
        { title: 'Pizza Paperoni', category: 'Pizza', rating: 4, image: 'https://foodhub.scene7.com/is/image/woolworthsltdprod/1905-meat-lovers-pizza:Desktop-1300x658', bgColor: '#E3F2FD' },
        { title: 'Pizza Meat', category: 'Pizza', rating: 3, image: 'https://png.pngtree.com/thumb_back/fh260/background/20241204/pngtree-a-delicious-pepperoni-pizza-perfect-for-sharing-image_16731493.jpg', bgColor: '#E0F7FA' },
        { title: 'Doner Kebab', category: 'Kebab', rating: 5, image: 'https://www.jocooks.com/wp-content/uploads/2023/04/chicken-doner-kebab-1.jpg', bgColor: '#E8F5E9' },
        { title: 'Salmon Roll', category: 'Salmon', rating: 4, image: 'https://i0.wp.com/www.craftycookbook.com/wp-content/uploads/2022/02/american-dream.png?resize=902%2C792&ssl=1', bgColor: '#FCE4EC' },
        { title: 'Cupcake Choco', category: 'Cupcake', rating: 4, image: 'https://bonnibakery.com/wp-content/uploads/2024/03/Chocolate-Cupcakes_52-1.jpg', bgColor: '#F1F8E9' },
        { title: 'Doughnut Milk', category: 'Doughnut', rating: 5, image: 'https://thumbs.dreamstime.com/b/pink-frosted-donuts-stacked-milk-bottle-pink-straw-napkin-four-pink-frosted-donuts-sprinkles-stacked-349982679.jpg', bgColor: '#FFF9C4' },
        { title: 'Doughnut Unicorn', category: 'Doughnut', rating: 4, image: 'https://i.pinimg.com/736x/f4/14/30/f41430be282a65e5f5bd3b45a27ed9f6.jpg', bgColor: '#F3E5F5' },
        { title: 'Kathi Kebab', category: 'Kebab', rating: 4, image: 'https://images.food52.com/mXqNblL1kbdItBsZy1lSbVmEknQ=/fit-in/1200x1200/a0247e36-ea75-4436-92ee-85a8009c32b2--2021-0427_kathi-kebab-roll_3x2_mark-weinberg-141.jpg', bgColor: '#E3F2FD' },
      ]
    };
  }
};
</script>

<style>
.card {
  border-radius: 12px;
}
.card-body {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
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

.floating-card-rating {
  color: #ffc107;
  font-size: 0.85rem;
}
</style>