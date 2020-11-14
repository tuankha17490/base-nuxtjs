<template>
  <div class="container main-content">
    <img
      class="icon"
      src="https://lh3.googleusercontent.com/proxy/chpZA9H_6oqUi2GX4c5xOiI3SaWt19uxBJOs1jYjQpgwJnn5MG2r3MjZmvIwMZH2vJOyQu6QDwtkfeGHNOyTPfkUuituqiibrp_HMslQbmjuTrW0AxE2TUf9aD6c_JvvG9EfQecXsEc"
      alt
    />
    <nuxt-link class="start" to="/sql-injection/start">LET'S START</nuxt-link>
  </div>
</template>
<script>
// import Logo from '~/components/Logo.vue'

export default {
  components: {
    // Logo
  },
  data() {
    return {
      show: true
    };
  }
};
</script>
<style>
.icon {
  width: 300px;
  height: 300px;
  display: block;
  margin: 50px 400px;
}
.start {
  color: white;
  display: block;
  text-align: center;
  background-color: chocolate;
  margin: 50px 420px;
  padding-bottom: 15px;
  padding-top: 15px;
  border-radius: 15px;
}
.start:hover {
  color: black;
}
</style>
