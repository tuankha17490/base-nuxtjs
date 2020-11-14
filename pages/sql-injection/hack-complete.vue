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
      <nuxt-link class="back" to="/sql-injection/third-login"
        >Back step</nuxt-link
      >
      <nuxt-link class="next" to="https://cudidi.herokuapp.com/"
        >Get demo</nuxt-link
      >
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
        And we are in! <p> successfully gained access to the application without having to guess the password, using <span>SQL INJECTION</span></p>
      </strong>

    </div>
    <div class="wrap-code">
      <div>
        <span>SELECT</span>* <br />
        <span>FROM</span> users<br />
        <span>WHERE</span> email = <span class="account"> 'user@email.com'</span
        ><br />
        <span>AND</span> pass = <span class="account"> ' ' <span> or </span> 1 = 1 - - ' </span
        >LIMiT 1<br />
      </div>
    </div>

  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style scoped>
.step-2 {
  margin-left: 0;
  margin-top: 100px;
}
.wrap-code {
  height: 180px;
  background-color: #000000c7;
  margin-top: 180px;
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
.step-2 span {
  color: #009fff;
}
</style>>



