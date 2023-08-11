<template>
  <div class="hero">
    <!-- Desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong> Delicious Food Menu,</strong> <br />
                in Your Gadget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit Anda!</p>
              <b-button variant="outline-success " size="sm">
                <b-icon-arrow-right></b-icon-arrow-right> Pesan sekarang
              </b-button>
            </div>
          </div>
        </div>
        <div class="col md-6">
          <img class="img-fluid" src="../assets/images/food-hero.png" />
        </div>
      </div>
    </div>
    <!--Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col md-6  mb-3">
          <img class="img-fluid" src="../assets/images/food-hero.png" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong> Delicious Food Menu,</strong> <br />
                in Your Gadget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit Anda!</p>
              <b-button variant="outline-success ">
                <b-icon-arrow-right></b-icon-arrow-right> Pesan
                sekarang</b-button
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroItems",
};
</script>

<style>
</style>