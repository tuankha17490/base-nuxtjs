<template>
  <div>
    <div class="main-image">
      <p></p>
    </div>
    <div class="container-fuild m-5 main-content">
      <div class="d-flex sql-injection">
        <img
          src="https://labs.septeni-technology.jp/wp-content/uploads/2016/05/sql-i%CC%A3nection.jpg"
          alt
        />
        <div>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          <a class="button" href="/sql-injection">TRY IT</a>
        </div>
      </div>
       <div class="d-flex xss">
           <div>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          <a class="button" href="/xss">TRY IT</a>
        </div>
        <img
          src="https://dpsvdv74uwwos.cloudfront.net/statics/img/ogimage/cross-site-scripting-xss.jpg"
          alt
        />
      </div>
    </div>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  components: {
    // Logo
  }
};
</script>

<style>
.main-image {
  background-image: url(https://willandway.vn/wp-content/uploads/2019/08/S%E1%BB%B1-kh%C3%A1c-bi%E1%BB%87t-gi%E1%BB%AFa-IT-Programmer-Coder-IT-Developer-v%C3%A0-K%E1%BB%B9-s%C6%B0-C%C3%B4ng-ngh%E1%BB%87-th%C3%B4ng-tin_willandway-2.jpg);
  background-size: cover;
  position: relative;
}
.main-image p {
  width: 100%;
  height: 700px;
}

.main-image::after {
  content: "";
  background-color: rgb(22 20 20 / 52%);
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.sql-injection {
  width: 100%;
  height: fit-content;
  margin-bottom: 100px;
  margin-top: 100px;
}
.sql-injection img {
  width: 800px;
  height: auto;
  opacity: 0.7;
}
.sql-injection div {
  width: 100%;
  height: fit-content;
  padding-right: 20px;
}
.sql-injection p {
  text-align: right;
  width: 95%;
  margin-left: 30px;
  font-size: x-large;
  margin-bottom: 70px;
}
.xss img {
  width: 800px;
  height: auto;
  opacity: 1;
}
.xss p {
  text-align: left;
  width: 95%;
  font-size: x-large;
  margin-bottom: 70px;
}
.button {
  background-color: #87bfc7;
  color: white;
  font-size: 20px;
  border-radius: 20px;
  padding: 15px 40px;
}
.sql-injection a {
  margin-left: 83%;
}
</style>
