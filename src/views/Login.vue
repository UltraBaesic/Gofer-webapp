<template>
  <main id="login">
    <div class="row">
      <div class="col-md-6 right-side">
        <div class="lb-header">
          <a
            href="#"
            class="login-link active"
            id="login-box-link"
            @click.prevent="setActive('login')"
            :class="{ active: isActive('login') }"
          >Login</a>
          <a
            href="#"
            class="register-link"
            id="register-box-link"
            @click.prevent="setActive('register')"
            :class="{ active: isActive('register') }"
          >Register</a>
        </div>

        <div class id>
          <div class="tab-pane fade" :class="{'active show': isActive('login')}">
            <div class="d-flex justify-content-center">
              <div>
                <form class="email-login">
                  <h1 class="login-header">Login</h1>
                  <p class="login-text">Enter your details and make sure protect your details from hackers</p>

                  <div class="col-xl-6 col-md-6" style="margin-top: 40px;">
                    <div class="section-headline margin-top-25 margin-bottom-12">
                      <h5 class="input-text">Email Address</h5>
                    </div>
                    <input class="input-box" placeholder />
                  </div>

                  <div class="col-xl-6 col-md-6" style="margin-top: 40px;">
                    <div class="section-headline margin-top-25 margin-bottom-12">
                      <h5 class="input-text">Password</h5>
                    </div>
                    <input class="input-box" placeholder />
                  </div>
                  <div class="password-block">
                    <a href="#" class="forgot-pass" @click.prevent>Forgot Password?</a>
                  </div>
                  <div id="checkbox">
                    <input type="checkbox" value="" class="checkboxme" v-model="rememberme" />

                    <label for="check">Remember me</label>
                  </div>
                  <div class="login-btn-block">
                    <a href="./errands.html" class="btn-login">Login</a>
                  </div>
                  <p class="account">
                    Don't have an account?
                    <a href="register" class="register-span-link">
                      <span class="register-span" id="register-span">Register</span>
                    </a>
                  </p>
                </form>
              </div>
            </div>
          </div>
        </div>

        <div class id>
          <div class="tab-pane fade" :class="{'active show': isActive('register')}">
            <div class="d-flex justify-content-center login">
              <div>
                <form class="email-signup">
                  <h1 class="login-header">Create an account</h1>
                  <p class="login-text">Fill in your details to register and start gofering</p>
                  <div class="account-input">
                    <div class="col-xl-3 col-md-3" style="margin-top: 20px;">
                      <div class="section-headline margin-top-25 margin-bottom-12">
                        <h5 class="input-text">First Name</h5>
                      </div>
                      <input class="input-box input-boxes" placeholder />
                    </div>

                    <div class="col-xl-3 col-md-3" style="margin-top: 20px;">
                      <div class="section-headline margin-top-25 margin-bottom-12 left-form">
                        <h5 class="input-text">Last Name</h5>
                      </div>
                      <input class="input-box input-boxes left-form" placeholder />
                    </div>
                  </div>
                  <div class="col-xl-6 col-md-6" style="margin-top: 20px;">
                    <div class="section-headline margin-top-25 margin-bottom-12">
                      <h5 class="input-text">Email Address</h5>
                    </div>
                    <input class="input-box" placeholder />
                  </div>

                  <div class="col-xl-6 col-md-6" style="margin-top: 20px;">
                    <div class="section-headline margin-top-25 margin-bottom-12">
                      <h5 class="input-text">Password</h5>
                    </div>
                    <input class="input-box" placeholder />
                  </div>

                  <div class="col-xl-6 col-md-6" style="margin-top: 20px;">
                    <div class="section-headline margin-top-25 margin-bottom-12">
                      <h5 class="input-text">Confirm Password</h5>
                    </div>
                    <input class="input-box" placeholder />
                  </div>
                  <div class="reg-btn-block" style="margin-top: 20px;">
                    <button class="btn-reg">Register</button>
                  </div>
                  <p class="account1" style="margin-top: 20px;">
                    Already registered
                    <a href="/errands.html" class="login-span-link">
                      <span class="login-span" id="login-span">Login</span>
                    </a>
                  </p>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-md-6 left-block">
        <div class="jumbotron bg-transparent text-white text-center">
          <img src="@/assets/img/auth-img.png" class="logo-image" alt="mobile view" />
          <h1 class="display text-header">Get stuffs Done for you.</h1>
          <p class="lead">
            A large network of people are available to run errands and
            <br />execute tasks for you.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      activeItem: "login",
      rememberme: false
    };
  },
  methods: {
    isActive(menuItem) {
      return this.activeItem === menuItem;
    },
    setActive(menuItem) {
      this.activeItem = menuItem;
    }
  }
};
</script>
 
<style scoped>
main {
  overflow-x: hidden !important;
}

/* LOGIN PAGE START */

.logo-image {
  width: 4rem;
  margin-top: 8rem;
}

.left-block {
  background-color: #eef6f9;
}

#login .left-block {
  background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("../assets/img/login-img.png");
  height: 100vh;
  background-position: center;
  background-size: cover;
}

.text-header {
  margin-top: 1rem;
  font-size: 30px;
}

.right-side {
  background-color: #eef6f9;
}

.login-block {
  margin-top: 80px;
}

.login-header {
  color: #0086b9;
  font-weight: 900;
  font-size: 38px;
  margin-bottom: 0px;
  margin-top: 30px;
  margin-left: 10px;
}

.lb-header {
  margin-top: 30px;
  margin-left: -9rem;
  text-align: center;
  justify-content: space-between;
}

.login-link,
.register-link {
  font-size: 16px;
  color: #0086b9;
  font-weight: 600;
}

.login-link {
  margin-right: 10rem;
}

.login-link:hover {
  text-decoration: none;
}

.forgot-pass {
  color: #0086b9;
}

.password-block {
  text-align: right;
  margin-right: 1rem;
}

.register-link:hover {
  text-decoration: none;
}

.register-link.active {
  text-decoration: none;
  color: #c8ccce;
  padding: 05px 1px;
  font-size: 14px;
}

.login-link.active {
  text-decoration: none;
  color: #c8ccce;
  padding: 05px 1px;
}

.login-text {
  margin-bottom: 0px;
  margin-left: 10px;
  color: #c8ccce;
}

.input-box {
  width: 30rem;
  padding: 0.7rem;
  border: 1px solid #c5eaf8;
}

.input-text {
  color: #c8ccce;
  font-size: 18px;
  font-weight: 600;
}

.login-btn-block {
  margin-left: 9rem;
  margin-top: 40px;
}

.btn-login {
  padding: 0.7rem 4rem;
  border-radius: 9px;
  color: #fff;
  background-color: #0086b9;
  border: none;
}

.btn-login:hover {
  padding: 0.7rem 4rem;
  border-radius: 9px;
  color: #fff !important;
  background-color: #0086b9;
  border: none;
  text-decoration: none;
}

.account {
  margin-top: 105px;
  margin-left: 7rem;
  color: #000000;
}

a .login-span {
  color: #0086b9;
}

a .login-span:hover {
  color: #0086b9;
}

.login-span-link:hover {
  text-decoration: none;
}

.email-login {
  margin-left: 90px;
}

.email-signup {
  margin-left: 90px;
  margin-top: -37.5rem;
}

/* Register  */

.register-block {
  margin-top: 40px;
}

.account-input {
  display: flex;
  justify-content: space-between;
}

.left-form {
  margin-left: -8rem;
}

.input-boxes {
  /* width: 20%; */
  padding: 0.7rem 0.8rem;
  width: 14rem;
}

.btn-reg {
  padding: 0.7rem 4rem;
  border-radius: 9px;
  color: #fff;
  background-color: #0086b9;
  border: none;
  outline: none;
}

.reg-btn-block {
  margin-left: 9rem;
}

.account1 {
  margin-left: 9rem;
  color: #000000;
}

a.register-span:hover {
  margin-left: 9rem;
  color: #0086b9;
  text-decoration: none !important;
}

.register-span-link:hover {
  text-decoration: none;
}

/* MEDIA QUERIES */

@media (max-width: 1024px) {
  /* Login & Register  */
  .email-login,
  .email-signup {
    margin-left: 45px;
  }

  .email-signup {
    margin-top: -34rem;
  }

  .lb-header {
    margin-right: 40px;
  }

  .login-link {
    margin-right: 06rem;
  }

  .input-box {
    width: 23rem;
    padding: 0.7rem 8rem;
    border: 1px solid #c5eaf8;
  }

  .login-btn-block,
  .reg-btn-block {
    margin-left: 6.5rem;
  }
  .account,
  .account1 {
    margin-left: 6rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 11rem;
  }

  .left-form {
    margin-left: -9rem;
  }
}

@media (max-width: 992px) {
  .email-login {
    margin-left: 15px;
  }

  .lb-header {
    margin-left: 125px;
  }

  .login-link {
    margin-right: 06rem;
  }

  .input-box {
    width: 20rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .login-btn-block {
    margin-left: 5.5rem;
    margin-top: 50px;
  }
  .account {
    margin-top: 50px;
    margin-left: 4rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 9rem;
  }

  .left-form {
    margin-left: -9rem;
  }

  .login-btn-block {
    margin-left: 5.5rem;
    margin-top: 50px;
  }

  .reg-btn-block {
    margin-left: 5rem;
  }
}

@media (max-width: 800px) {
  /* Login & Register  */
  .email-login {
    margin-left: 15px;
  }

  .email-signup {
    margin-left: 15px;
    margin-top: -33rem;
  }

  .lb-header {
    margin-left: 25px;
  }

  .input-box {
    width: 20rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .login-btn-block {
    margin-left: 5.5rem;
    margin-top: 50px;
  }
  .account {
    margin-left: 6rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 9rem;
  }

  .left-form {
    margin-left: -6rem;
  }

  .reg-btn-block {
    margin-left: 5rem;
  }
}

@media (max-width: 767px) {
  .left-form {
    margin-left: -7.5rem;
  }

  .lb-header {
    margin-left: 100px;
  }

  .email-login {
    margin-left: 90px;
  }

  .email-signup {
    margin-left: 90px;
    margin-top: -30rem;
  }

  .left-side {
    display: none;
  }

  .input-box {
    width: 30rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .login-btn-block {
    margin-left: 9.5rem;
    margin-top: 50px;
  }

  .account {
    margin-top: 50px;
    margin-left: 7rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 14.5rem;
  }

  .left-form {
    margin-left: -5.5rem;
  }

  .reg-btn-block {
    margin-left: 9rem;
  }

  .account1 {
    margin-left: 9rem;
  }
}

@media (max-width: 666px) {
  .email-signup {
    margin-left: 80px;
  }
  .lb-header {
    margin-left: 90px;
  }
  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 13.5rem;
  }

  .left-form {
    margin-left: -2rem;
  }

  .reg-btn-block {
    margin-left: 9rem;
  }

  .account1 {
    margin-left: 9rem;
  }
}

@media (max-width: 576px) {
  .account {
    margin-top: 50px;
    margin-left: 6rem;
  }

  .input-box {
    width: 22rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 9.5rem;
  }

  .left-form {
    margin-left: -3rem;
  }

  .reg-btn-block {
    margin-left: 6rem;
  }

  .login-btn-block {
    margin-left: 6rem;
  }

  .account1 {
    margin-left: 6rem;
  }

  .email-signup {
    margin-left: 80px;
    margin-top: -35rem;
  }

  .email-login {
    margin-left: 80px;
  }

  .lb-header {
    margin-left: 90px;
  }
}

@media (max-width: 414px) {
  .input-box {
    width: 20rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .email-login {
    margin-left: 25px;
    margin-top: 2rem;
  }

  .email-signup {
    margin-left: 25px;
    margin-top: -32.5rem;
  }

  .lb-header {
    margin-right: 25px;
  }

  .login-link {
    margin-right: 3rem;
  }

  .login-btn-block {
    margin-left: 5.5rem;
    margin-top: 50px;
  }

  .left-form {
    margin-left: -18px;
  }

  .account {
    margin-top: 50px;
    margin-left: 4rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 9.7rem;
  }

  .reg-btn-block {
    margin-left: 5rem;
  }
  .account1 {
    margin-left: 5rem;
  }
}

@media (max-width: 410px) {
  .input-box {
    width: 20rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 9.9rem;
  }

  .email-login {
    margin-left: 25px;
  }
  /* .email-signup {
    margin-top: -31rem;
  } */

  .sign-upp {
    margin-top: -1rem;
  }

  .lb-header {
    margin-left: 35px;
  }

  .login-btn-block {
    margin-left: 5.5rem;
    margin-top: 50px;
  }

  .account {
    margin-top: 50px;
    margin-left: 4rem;
  }
}

@media (max-width: 375px) {
  .account {
    margin-top: 50px;
    margin-left: 2rem;
  }
  .input-box {
    width: 17rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .login-btn-block {
    margin-left: 4rem;
    margin-top: 50px;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 7.9rem;
  }

  .left-form {
    margin-left: -1.5rem;
  }

  .reg-btn-block {
    margin-left: 3.5rem;
  }
  .account1 {
    margin-left: 3.5rem;
  }
}

@media (max-width: 360px) {
  .input-box {
    width: 17rem;
    padding: 0.7rem 1rem;
    border: 1px solid #c5eaf8;
  }

  .email-login {
    margin-left: 20px;
  }

  /* .email-signup {
    margin-top: -36rem;
  } */

  .lb-header {
    margin-left: 30px;
  }

  .login-btn-block {
    margin-left: 4.5rem;
    margin-top: 50px;
  }

  .account {
    margin-top: 50px;
    margin-left: 2rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 7.9rem;
  }

  .left-form {
    margin-left: -1.5rem;
  }

  .login-header {
    font-size: 28px;
  }
}

@media (max-width: 320px) {
  .input-box {
    padding: 0.7rem 1rem;
    border-radius: 6px;

    width: 15rem;
  }

  .email-login {
    margin-left: 25px;
  }

  .email-signup {
    margin-top: -32rem;
  }

  .lb-header {
    margin-left: 35px;
  }

  .login-btn-block {
    margin-left: 3.5rem;
    margin-top: 50px;
  }

  .account {
    margin-top: 50px;
    margin-left: 1rem;
  }

  .input-boxes {
    padding: 0.7rem 0.8rem;
    width: 7rem;
  }

  .left-form {
    margin-left: rem;
  }

  .reg-btn-block {
    margin-left: 2.5rem;
  }

  .account1 {
    margin-left: 2.5rem;
  }
}
</style>