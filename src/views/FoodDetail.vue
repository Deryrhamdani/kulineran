<template>
  <div class="food-detail">
    <Navbar />
    <div class="container mb-5">
      <!-- breadcrumb -->
      <div class="row mt-5">
        <div class="col">
          <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
              <li class="breadcrumb-item">
                <router-link to="/" class="text-dark">Home</router-link>
              </li>
              <li class="breadcrumb-item">
                <router-link to="/foods" class="text-dark">Foods</router-link>
              </li>
              <li class="breadcrumb-item active" aria-current="page">
                Food Order
              </li>
            </ol>
          </nav>
        </div>
      </div>
      <!-- breadcrumb -->
      <div class="row mt-2">
        <div class="col md-6">
          <img
            class="card-img-top card h-100 img-fluid shadow"
            :src="'../images/' + product.gambar"
            alt="Card image cap"
          />
        </div>
        <div class="col md-6 mt-2">
          <h2>
            <strong>{{ product.nama }}</strong>
            <hr />
            <h4>
              Harga Rp : <b>{{ formatPrice(product.harga) }}</b>
            </h4>
            <form>
              <div class="form-group mt-2 mb-2 text-standar">
                <input
                  type="number"
                  class="form-control"
                  id="jumlah_pesamam"
                  aria-describedby="JumlahPesanan"
                  placeholder="Jumlah Pesanan"
                />
              </div>
              <div class="form-group">
                <textarea
                  class="form-control"
                  placeholder="Keterangan spt : Pedas, Nasi setengah..."
                  id="textarea"
                ></textarea>
                <button type="submit" class="btn btn-success float-end mt-3">
                  <b-icon-cart></b-icon-cart>
                  Pesan
                </button>
              </div>
            </form>
          </h2>
        </div>
      </div>
    </div>
    <Footer />
    <Copyright />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Copyright from "@/components/Copyright.vue";
import Footer from "@/components/Footer.vue";
import axios from "axios";
export default {
  name: "FoodDetailItems",
  components: {
    Navbar,
    Footer,
    Copyright,
  },
  data() {
    return {
      product: [],
    };
  },
  methods: {
    formatPrice(value) {
      let val = (value / 1).toFixed().replace(".", ",");
      return val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
    },
    setProduct(data) {
      this.product = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/products/" + this.$route.params.id)
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
.text-standar {
  font-size: 18px;
}
</style>