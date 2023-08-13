<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="row mt-4">
        <div class="col">
          <h2>Daftar <strong>Makanan</strong></h2>
        </div>
      </div>
      <div class="row mt-3">
        <div class="col">
          <div class="input-group mb-3">
            <input
              v-model="search"
              type="text"
              class="form-control"
              placeholder="Cari makanan kesukaan Anda"
              aria-label="Cari"
              aria-describedby="button-addon2"
              @keyup="searchFood"
            />
            <div class="input-group-append">
              <button
                class="btn btn-outline-secondary"
                type="button"
                id="button-addon2"
              >
                <b-icon-search></b-icon-search>
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="row mt-2 row-cols-md-4 g-4">
        <div
          class="col md- mt-4 mb-3"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
      <Footer />
      <Copyright />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
import Copyright from "@/components/Copyright.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "FoodView",
  components: {
    Navbar,
    Footer,
    CardProduct,
    Copyright,
  },
  data() {
    return {
      products: [],
      search: "",
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },

    searchFood() {
      axios
        .get("http://localhost:3000/products?q=" + this.search)
        .then((response) => this.setProduct(response.data))
        .catch((error) => console.log(error));
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/products")
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

