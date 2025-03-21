<template>
  <div>
    <!-- Footer Default (Desktop) -->
    <footer v-if="!isMobile" class="footer mt-5 p-4">
      <div class="container main-container">
        <div class="row">
          <!-- Logo dan alamat -->
          <div class="col-md-4 text-section">
            <a class="navbar-brand d-flex align-items-center" href="#">
              <div class="text-start">
                <h2 class="text-primary">elemes.<span class="text-dark">id</span></h2>
                <p class="fs-6 text-muted mb-0 d-none d-md-block">Product and Tech Agency Company</p>
              </div>
            </a>
            <p class="text-start">
              Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan, Kecamatan Setiabudi, 
              Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12950
            </p>
            <div class="social-icons">
              <font-awesome-icon class="contact-icon" :icon="['fas', 'envelope']" />
              <font-awesome-icon class="contact-icon" :icon="['fas', 'phone']" />
              <font-awesome-icon class="contact-icon" :icon="['fab', 'instagram']" />
            </div>
          </div>

          <!-- Categories -->
          <div class="col-md-2 text-section">
            <h5>Categories</h5>
            <ul class="list-unstyled text-start">
              <li><a href="#">Cupcake</a></li>
              <li><a href="#">Pizza</a></li>
              <li><a href="#">Kebab</a></li>
              <li><a href="#">Salmon</a></li>
              <li><a href="#">Doughnut</a></li>
            </ul>
          </div>

          <!-- About Us -->
          <div class="col-md-2 text-section">
            <h5>About Us</h5>
            <ul class="list-unstyled text-start">
              <li><a href="#">About Us</a></li>
              <li><a href="#">FAQ</a></li>
              <li><a href="#">Report Problem</a></li>
            </ul>
          </div>

          <!-- Newsletter -->
          <div class="col-md-4 text-section">
            <h5>Newsletter</h5>
            <p class="text-start">Get now free 50% discount for all products on your first order</p>
            <div class="input-group mb-3">
              <input type="email" class="form-control" placeholder="Your email address">
              <button class="btn btn-success">SEND</button>
            </div>
            <p><i class="bi bi-envelope"></i> elemesid@gmail.com</p>
            <p><i class="bi bi-telephone"></i> 0888 1111 2222</p>
          </div>
        </div>
      </div>
    </footer>

    <!-- Footer Mobile -->
    <div v-else class="footer-mobile">
      <div class="menu">
        <div class="menu-item">
          <div class="icon">☰</div>
          <div class="label">Home</div>
        </div>
        <div class="menu-item">
          <div class="icon">☰</div>
          <div class="label">Promotions</div>
        </div>
        <div class="menu-item">
          <div class="icon">☰</div>
          <div class="label">Others</div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faInstagram } from "@fortawesome/free-brands-svg-icons";
import { faEnvelope, faPhone } from "@fortawesome/free-solid-svg-icons";
library.add(faEnvelope, faPhone, faInstagram);

export default {
  name: "footerSection",
  data() {
    return {
      isMobile: window.innerWidth <= 768, // Deteksi apakah layar mobile atau tidak
    };
  },
  mounted() {
    window.addEventListener("resize", this.checkScreenSize);
  },
  beforeUnmount() { // Ganti dari beforeDestroy ke beforeUnmount
    window.removeEventListener("resize", this.checkScreenSize);
  },
  methods: {
    checkScreenSize() {
      this.isMobile = window.innerWidth <= 768;
    },
  },
  components: {
    FontAwesomeIcon,
  },
};
</script>


<style scoped>
.footer {
  background-color: #f6fdeb;
  border-radius: 10px;
}

.footer-mobile {
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: fixed;
  bottom: 0;
  width: 100%;
  background: white;
  padding: 10px 0;
  border-top: 1px solid #ddd;
}

.menu {
  display: flex;
  justify-content: space-around;
  width: 100%;
}

.menu-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: gray;
}

.icon {
  font-size: 20px;
}

h5 {
  font-weight: bold;
}

ul li a {
  text-decoration: none;
  color: #555;
}

ul li a:hover {
  color: #8fc63d;
}

.text-section {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.contact-icon {
  font-size: 32px;
  margin: 0px 10px 10px 10px;
}
</style>


