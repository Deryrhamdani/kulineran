<template>
    <div>
      <Navbar />
      <h2>Keranjang</h2>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import Navbar from "@/components/Navbar.vue";
  
  export default {
    name: "KeranjangView",
    components: {
      Navbar,
    },
  };
  </script>