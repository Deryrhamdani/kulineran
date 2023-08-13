<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />
      <div class="row mt-5">
        <div class="col">
          <h2>Best <strong> Foods</strong></h2>
        </div>
        <div class="col">
          <router-link to="/foods" class="btn btn-success float-end"
            >Lihat Semua
          </router-link>
        </div>
        <div class="row mb-4 gridWrap">
          <div
            class="col md-4 mt-4 g-3"
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
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import Footer from "@/components/Footer.vue";
import Copyright from "@/components/Copyright.vue";
import axios from "axios";

export default {
  name: "HomeView",
  components: {
    Navbar,
    Hero,
    CardProduct,
    Footer,
    Copyright,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/best-products")
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
.gridWrap {
  width: 1024px;
  margin: auto;
}

.gridWrap ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 25px;
  justify-content: center;
  list-style: none;
  padding-left: 0;
}

.gridWrap ul img {
  width: 100%;
}</style>