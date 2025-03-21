<template>
  <footer class="footer mt-5 p-4">
    <div class="container">
      <div class="row">
        <!-- Logo dan alamat -->
        <div class="col-md-4">
          <img src="@/assets/logo.png" alt="elemes.id" class="mb-3">
          <p class="text-muted">
            Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan, Kecamatan Setiabudi, 
            Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12950
          </p>
          <div class="social-icons">
            <a href="#" class="icon"><i class="bi bi-envelope"></i></a>
            <a href="#" class="icon"><i class="bi bi-telephone"></i></a>
            <a href="#" class="icon"><i class="bi bi-instagram"></i></a>
          </div>
        </div>

        <!-- Categories -->
        <div class="col-md-2">
          <h5>Categories</h5>
          <ul class="list-unstyled">
            <li><a href="#">Cupcake</a></li>
            <li><a href="#">Pizza</a></li>
            <li><a href="#">Kebab</a></li>
            <li><a href="#">Salmon</a></li>
            <li><a href="#">Doughnut</a></li>
          </ul>
        </div>

        <!-- About Us -->
        <div class="col-md-2">
          <h5>About Us</h5>
          <ul class="list-unstyled">
            <li><a href="#">About Us</a></li>
            <li><a href="#">FAQ</a></li>
            <li><a href="#">Report Problem</a></li>
          </ul>
        </div>

        <!-- Newsletter -->
        <div class="col-md-4">
          <h5>Newsletter</h5>
          <p>Get now free 50% discount for all products on your first order</p>
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
</template>

<style scoped>
.footer {
  background-color: #f6fdeb;
  border-radius: 10px;
}

.social-icons .icon {
  display: inline-block;
  margin-right: 10px;
  padding: 10px;
  background-color: #8fc63d;
  border-radius: 50%;
  color: white;
  text-decoration: none;
}

.social-icons .icon:hover {
  background-color: #6a9e2c;
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
</style>


<script>


export default {
  name: 'footerSection',
  props: {
    msg: String
  }
}
</script>
