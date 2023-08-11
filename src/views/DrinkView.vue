<template>
  <div>
    <Navbar />
    <div class="container mt-5">
      <h2>Daftar Minuman</h2>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";

export default {
  name: "DrinkView",
  components: {
    Navbar,
  },
};
</script>