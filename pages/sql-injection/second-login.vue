<template>
  <div class="container main-content">
    <div class="wrap">
      <iframe
        id="frame"
        src="https://www.hacksplaining.com/embedded/sql-injection/"
        width="100%"
        height="100%"
        scrolling="no"
      ></iframe>
    </div>
    <div class="wrap-button d-flex justify-content-between">
      <nuxt-link class="back" to="/sql-injection/first-login">Back step</nuxt-link>
      <nuxt-link class="next" to="/sql-injection/introducing-code">Next step</nuxt-link>
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
        Okay, so guessing the password didn't work.<span>Let's try adding a quote character after the password:</span>
        <div class="login">
          <div class="row">
            <div class="field">Email:</div>
            <div class="value">user@email.com</div>
          </div>
          <div class="row">
            <div class="field">Password:</div>
            <div class="value">password'</div>
          </div>
        </div>
      </strong>
    </div>
      <div class="step-3">
      <strong>Hmmmmm.<span>The application crashed with an unexpected error.</span></strong>
    </div>
  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style scoped>
.login {
  margin-top: 10px;
}
.field {
  margin-left: 20px;
}
.value {
  margin-left: 15px;
  font-weight: lighter;
  color: gray;
}
strong {
  margin-left: 0;
}
.step-2 {
  margin-left: 0;
  margin-top: 100px;
}
.wrap iframe,
.fade {
  margin-left: 350px;
  margin-top: 120px;
}

.wrap-log iframe,
.log {
  height: 180px;
  width: 800px;
  margin-left: 250px;
  margin-top: 400px;
}
.log {
  opacity: 0.4;
}
.step-3 {
  margin-top: 400px;
  margin-left: 300px;
}
</style>>



