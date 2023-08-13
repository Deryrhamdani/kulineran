<template>
  <div class="col g-4">
    <div class="card shadow card-product">
      <img
        class="card-img-top card h-100 img-fluid"
        :src="'images/' + product.gambar"
        alt="Card image cap"
      />
      <div class="card-body">
        <h6 class="card-title">{{ product.nama }}</h6>
        <p class="card-text">Harga : Rp {{ formatPrice(product.harga) }}</p>
        <router-link :to="'/foods/' + product.id" class="btn btn-success"
          ><b-icon-cart></b-icon-cart> Pesan</router-link
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: " CardProduct",
  props: ["product"],

  methods: {
    formatPrice(value) {
      let val = (value / 1).toFixed().replace(".", ",");
      return val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
    },
  },
};
</script>

<style>
/* .img-fluid {
  max-width: 100%;
  height: auto;
} */

.card-style {
  margin: auto;
  width: 80%;
  padding: 10px;
}
.card-img-top {
  margin: auto;
  width: 30%;
}
.card-title {
  text-align: left;
}
.card-footer {
  background-color: #fff;
}
.rounded {
  border-radius: 0.6rem !important;
}
.rounded-bottom {
  border-bottom-left-radius: 0.6rem !important;
  border-bottom-right-radius: 0.6rem !important;
}
.card-text {
  text-align: justify;
  font-size: 100%;
}
</style>

