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
      <nuxt-link class="back" to="/sql-injection/second-login">Back step</nuxt-link>
      <nuxt-link class="next" to="/sql-injection/third-login">Next step</nuxt-link>
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
    <div class="wrap-code">
      <div>
        <span>SELECT</span>* <br>
        <span>FROM</span>  users<br>
        <span>WHERE</span>  email = <span class="account"> 'user@email.com'</span><br>
        <span>AND</span>  pass = <span class="account"> 'password'' LIMiT 1</span><br>
      </div>
    </div>
      <div class="step-3">
      <strong>The quote is inserted directly into the SQL string, and terminates the query early. <span>This is what caused the syntax error we saw in the logs</span></strong>
    </div>
  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style scoped>
.wrap-code {
  height: 180px;
  background-color: #000000c7;
  margin-top: 420px;
  margin-left: 550px;
}
.wrap-code div {
  color: #ffffff;
  margin-left: 30px;
  padding-top: 20px;
  font-size: 14px;
}
.wrap-code span {
  color: green;
  margin-right: 5px;
}
.wrap-code .account {
  color: rgb(187, 150, 221);
  margin-left: 5px;
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
  width: 400px;
  margin-left: 0;
}
.wrap iframe,
.fade {
  margin-left: 350px;
  margin-top: 120px;
}

.wrap-log iframe,
.log {
  height: 180px;
  width: 500px;
  margin-left: 30px;
  margin-top: 400px;
}
.log {
  opacity: 0.4;
}
.step-3 {
  margin-top: 10px;
  margin-left: 600px;
}
</style>>



