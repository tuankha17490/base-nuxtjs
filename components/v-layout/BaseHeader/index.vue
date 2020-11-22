/* eslint-disable vue/html-self-closing */
<template>
  <header class="d-flex justify-content-center align-items-center my-2 mx-3 ">
    <a href="/" class="brand-title">HACKINGLESSON</a>
    <a-menu mode="horizontal" class="menu">
      <a-menu-item class="menu-item" key="home">
        <nuxt-link to="/">HOME</nuxt-link>
      </a-menu-item>
      <a-menu-item class="menu-item" key="sql-injection">
        <nuxt-link to="/sql-injection">SQL INJECTION</nuxt-link>
      </a-menu-item>
      <a-menu-item class="menu-item" key="xss">
        <nuxt-link to="/xss">CROSS-SITE SCRIPTING</nuxt-link>
      </a-menu-item>
      <a-menu-item class="menu-item" key="demo">
        <a href="https://cudidi.herokuapp.com/">DEMO</a>
      </a-menu-item>
    </a-menu>
  </header>
</template>

<style scoped>
@import url("./style.scss");
</style>

<script>
export default {
  name: "BaseHeader",
  props: {},

  methods: {
    loggOut() {
      this.$store.dispatch("auth/signOut", { vue: this });
    }
  }
};
</script>
