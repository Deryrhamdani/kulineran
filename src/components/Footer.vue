<template>
  <div
    class="container-fluid bg-dark footer  wow fadeIn"
    data-wow-delay="0.1s"
  >
    <div class="container py-5">
      <div class="row g-5">
        <div class="col-lg-4 col-md-6">
          <h4 class="text-white mb-4">Kantor Kami</h4>
          <p class="mb-2">
            <i class="fa fa-map-marker-alt me-3"></i><strong>Kebun Raya Bogor</strong>
          </p>
          <p class="mb-2">
            <i class="fa fa-map-marker-alt me-3"></i>Bogor, Jawa Barat-Indonesia
          </p>
          <p class="mb-2"><i class="fa fa-phone-alt me-3"></i>+62 5345 67890</p>
          <p class="mb-2"><i class="fa fa-envelope me-3"></i>csdbs.com</p>
          <div class="d-flex pt-3">
            <a
              class="animated-button btn btn-square btn-light rounded-circle me-2"
              href=""
              ><i class="fas fa-map-marker-alt text-dark"></i
            ></a>
            <a
              class="animated-button btn btn-square btn-light rounded-circle me-2"
              href=""
              ><i class="fab fa fa-phone-alt text-dark"></i
            ></a>
            <a
              class="animated-button btn btn-square btn-light rounded-circle me-2"
              href=""
              ><i class="fa fa-envelope text-dark"></i
            ></a>
            <a
              class="animated-button btn btn-square btn-light rounded-circle me-2"
              href=""
              ><i class="fab fa-instagram text-dark"></i
            ></a>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <h4 class="text-white mb-4">Kantor Kami</h4>
          
          <a class="btn btn-link" href="">Bogor</a>
          <a class="btn btn-link" href="">Cibodas</a>
          <a class="btn btn-link" href="">Purwodadi</a>
          <a class="btn btn-link" href="">Bali</a>
        </div>
        <div class="col-lg-4 col-md-6">
          <img
            class="img-fluid text-white"
            src="../assets/images/food-hero.png"
            alt="Icon"
            style="height: 40px"
          />
          <p></p>
          <a class="btn btn-link" href="">Projects</a>
          <a class="btn btn-link" href="">Kontak</a>
          <a class="btn btn-link" href="">Tentang Kami</a>
          <a class="btn btn-link" href="">FAQ</a>
        </div>
      </div>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "footerItems",
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
};
</script>
  
  <style scoped>
.footer {
  color: #b0b9ae;
}

.footer .btn.btn-link {
  display: block;
  margin-bottom: 5px;
  padding: 0;
  text-align: left;
  color: #b0b9ae;
  font-weight: normal;
  text-transform: capitalize;
  transition: 0.3s;
  text-decoration: none;
}

.footer .btn.btn-link::before {
  position: relative;
  content: "\f105";
  font-family: "Font Awesome 5 Free";
  font-weight: 900;
  margin-right: 10px;
}

.footer .btn.btn-link:hover {
  color: var(--light);
  letter-spacing: 1px;
  box-shadow: none;
}
</style>
  