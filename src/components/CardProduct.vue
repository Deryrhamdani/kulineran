<template>
  <div class="card shadow card-product">
    <img
      class="card-img-top"
      :src="'images/' + product.gambar"
      alt="Card image cap"
    />
    <div class="card-body">
      <h5 class="card-title">{{ product.nama }}</h5>
      <p class="card-text">Harga : Rp {{ product.harga }}</p>
      <a href="#" class="btn btn-success"><b-icon-cart></b-icon-cart> Pesan</a>
    </div>
  </div>
</template>

<script>
export default {
  name: " CardProduct",
  props: ["product"],
};
</script>

<style>
</style>