<template>
  <div class="container main-content">
    <img
      class="icon"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Note_icon.svg/1200px-Note_icon.svg.png"
      alt
    />
    <nuxt-link class="start" to="/xss/start">LET'S START</nuxt-link>
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
