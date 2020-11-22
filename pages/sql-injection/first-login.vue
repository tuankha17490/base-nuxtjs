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
      <nuxt-link class="back" to="/sql-injection/introduce-log">Back step</nuxt-link>
      <nuxt-link class="next" to="/sql-injection/second-login">Next step</nuxt-link>
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
        Go ahead and try logging in with the following credentials:
        <div class="login">
          <div class="row">
            <div class="field">Email:</div>
            <div class="value">user@email.com</div>
          </div>
          <div class="row">
            <div class="field">Password:</div>
            <div class="value">password</div>
          </div>
        </div>
      </strong>
    </div>
    <div class="step-3">
      <strong>You will see not find user account in here.<span> Invalid Credentials</span></strong>
    </div>
  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style scoped>
strong {
  width: 300px;
  height: fit-content;
  display: block;
  margin-left: 200px;
  font-size: initial;
  background-color: burlywood;
  padding: 15px;
  border-radius: 25px;
}
strong span {
  font-weight: lighter;
}
.step-2 {
  margin-top: 600px;
  margin-left: 400px;
}
.wrap iframe,
.fade {
  margin-left: 200px;
  margin-top: 220px;
}
.fade,
iframe {
  width: 700px;
  height: 320px;
  top: 0;
  left: 0;
}
.fade {
  position: absolute;
  background-color: #333;
  opacity: 0.6;
  z-index: 10;
}
iframe {
  overflow: hidden;
  border: none;
  position: absolute;
}
.wrap,
.wrap-log {
  position: relative;
}
.back,
.next {
  background: rgba(250, 173, 20, 0.2);
  padding: 15px;
  border: none;
  cursor: pointer;
  border-radius: 10px;
  color: #333;
}

.next:hover,
.back:hover {
  color: white;
  background-color: #333;
  opacity: 0.7;
}
.wrap-button {
  margin-top: 20px;
  margin-bottom: 20px;
}
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
.step-3 span {
  color: red;
}
</style>>



