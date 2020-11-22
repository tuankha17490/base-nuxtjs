<template>
  <div class="container main-content">
    <div class="wrap">
      <iframe
        src="https://www.hacksplaining.com/embedded/sql-injection/"
        width="100%"
        height="100%"
        scrolling="no"
      ></iframe>
      <div class="fade"></div>
    </div>
    <div class="wrap-button d-flex justify-content-between">
      <nuxt-link class="back" to="/sql-injection/start">Back step</nuxt-link>
      <nuxt-link class="next" to="/sql-injection/first-login">Next step</nuxt-link>
    </div>
    <div class="wrap-log">
      <iframe
        src="https://www.hacksplaining.com/embedded/sql-injection/logs"
        width="100%"
        height="100%"
        scrolling="no"
      ></iframe>
      <div class="fade log"></div>
    </div>
    <div class="step-2">
      <strong>
        Here are the application logs.
        <span>
          Watch what happens here when you interact with the
          vulnerable application.
        </span>
      </strong>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style scoped>
.wrap iframe, .fade {
  margin-left: 200px;
  margin-top: 120px;
}

.wrap-log iframe, .log {
  height: 180px;
  width: 800px;
  margin-left: 200px;
  margin-top: 370px;
}
.log {
  opacity: 0.4;
}

</style>>



