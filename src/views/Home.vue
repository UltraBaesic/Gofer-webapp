<template>
  <main id="home">
    <section class="hero-section">
      <nav-bar></nav-bar>
      <div class="banner">
        <div class="jumbotron bg-transparent text-white text-center">
          <h1 class="display-4">Get someone to do your tasks for you</h1>
          <p class="lead">
            Get connected to someone who can run your errands for you while you do your thing. You can run just any type of errand.
            <span
              class="start-now"
            >Start Now</span>
          </p>
          <div class="images">
            <img class="mobile-img1" src="@/assets/img/appstore.png" alt="appstore" />
            <img class="mobile-img" src="@/assets/img/playstore.png" alt="appstore" />
          </div>
        </div>
      </div>
    </section>
    <section class="tab-section">
      <div class="tab-container">
        <div class="tab-list">
          <ul class="nav nav-tabs nav-justified">
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('post')"
                :class="{ active: isActive('post') }"
                href="#post"
              >Post Errands</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('run')"
                :class="{ active: isActive('run') }"
                href="#run"
              >Run Errands</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('get')"
                :class="{ active: isActive('get') }"
                href="#get"
              >Get Verified</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('join')"
                :class="{ active: isActive('join') }"
                href="#join"
              >Join us</a>
            </li>
          </ul>
          <div class="tab-content py-3" id="myTabContent">
            <div class="tab-pane fade" :class="{'active show': isActive('post')}">
              <div class="d-flex justify-content-center post">
                <div>
                  <h4>What Kind of Errand do you want done?</h4>
                  <p>The type of errand you can post is absolutely limitless, if you can think it you can post. you can get started and start posting, select a category below to start posting</p>
                  <post-errands></post-errands>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="first-errand-section">
      <div class="first-post-section">
        <div class="container">
          <div class="row section-post-first">
            <div class="col-md-6 image-block">
              <img
                src="@/assets/img/image2.jpeg"
                class="img-fluid post-imagee"
                alt="Responsive image"
              />
            </div>
            <div class="col-md-6">
              <div class="intro">
                <h1 class="post-errand-head post-errand-head-extend">
                  <span class="inner-heading">Post Your Errand</span> and let
                  <br />someone do it for you
                </h1>
                <p class="post-errand-paragraph">
                  You don't have to do all the work by yourself, let someone ease you off the stress
                  <a
                    href="wallet.html"
                    class="app-link"
                  >Download the Gofer App</a> now and start sending errands.
                </p>
                <!-- <a href="#" class="btn btn-primary">Show me how</a> -->
              </div>
              <div class="post-list">
                <ul class="post-errand-list">
                  <li>Describe the errand and the reward for the errand</li>
                  <li>Wait for someone to bid or negotiate</li>
                  <li>Accept or reject bids</li>
                  <li>Track errand and end errand after errand is successful</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="second-errand-section">
      <div class="second-post-section">
        <div class="second-block">
          <div class="container">
            <div class="row section-post-second">
              <div class="col-md-6">
                <div class="intro">
                  <h1 class="post-errand-head">
                    <span class="inner-heading">Run Errands</span> for people
                    <br />and earn cash
                  </h1>
                  <p
                    class="post-errand-paragraph"
                  >Search and bid for errands that you would like to run. Run errands and earn money after successful completion of the errand</p>
                </div>
                <div class="post-list">
                  <ul class="post-errand-list">
                    <li class="list-item-post">Search and bid for errands</li>
                    <li class="list-item-post">Wait to be accepted by the sender</li>
                    <li class="list-item-post">Run errand and end errand after completion</li>
                    <li class="list-item-post">Earn Money</li>
                  </ul>
                </div>
              </div>

              <div class="col-md-6 image-block">
                <img
                  src="@/assets/img/image2.jpeg"
                  class="img-fluid post-image"
                  alt="Responsive image"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="third-section">
      <div class="Third-post-section">
        <div class="container">
          <div class="row section-post-third">
            <div class="col-md-6 image-block">
              <img
                src="@/assets/img/image2.jpeg"
                class="img-fluid post-imagee"
                alt="Responsive image"
              />
            </div>
            <div class="col-md-6">
              <div class="intro">
                <h1 class="post-errand-head post-errand-head-extend-1">
                  <span class="inner-heading">Join us</span>, be part of the
                  <br />team that run errands
                  <br />for us
                </h1>
                <p
                  class="post-errand-paragraph"
                >Running errands for us comes with special privileges. To join our team of errand runners you have to apply to be a special errand runner and all errands directed to Gofer will be assigned to our different errand runners in different regions</p>
                <a href="#" class="btn btn-primary btn-apply">Apply Now</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="wallet">
      <div class="wallet-section">
        <div class="container section-wallet">
          <div class="row">
            <hr class="wallet-line" />
            <h1 class="wallet-heading inner-heading">Wallet</h1>
          </div>

          <div class="row">
            <div class="col-md-4">
              <div class="wallet-card">
                <div class="illustration-box">
                  <img src="@/assets/img/mask.png" class="illustration" alt="record illustration" />
                </div>
                <div class="wallet-body">
                  <h3 class="pri-text">My Wallet</h3>
                  <p
                    class="sec-text"
                  >Post an errand with all the details needed to run the errand and the amount you are willing to pay errand.</p>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="wallet-card">
                <div class="illustration-box">
                  <img src="@/assets/img/mask.png" class="illustration" alt="share illustration" />
                </div>
                <div class="wallet-body">
                  <h3 class="pri-text">Wallet Pin</h3>
                  <p
                    class="sec-text"
                  >Post an errand with all the details needed to run the errand and the amount you are willing to pay errand.</p>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="wallet-card">
                <div class="illustration-box">
                  <img src="@/assets/img/mask.png" class="illustration" alt="voila illustration" />
                </div>
                <div class="wallet-body">
                  <h3 class="pri-text">Escrow Account</h3>
                  <p
                    class="sec-text"
                  >Post an errand with all the details needed to run the errand and the amount you are willing to pay errand.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="review-section">
        <div class="container">
          <div class="row p-5">
            <div class="col-md-6 text-center">
              <img
                src="@/assets/img/image2.jpeg"
                class="post-image post-image-fourth"
                alt="mobile view"
              />
            </div>
            <div class="col-md-6 account-reviews intro pt-4">
              <h3 class="post-errand-head">Account Reviews and account verification</h3>
              <p class="post-errand-paragraph">
                Post an errand with all the details needed to run the errand and the amount you are willing
                to pay errand runner. wait for runners to bid and then accept a runner based on review
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="get-started-outer">
        <div class="container">
          <div class="row p-5 get-started">
            <div class="get-it">
              <div class="col-xs-6 get-started-inside">
                <div class="get-started-text">Start Posting Errands and Running Errands</div>
              </div>
              <div class="col-xs-6 get-started-btn-block">
                <button class="get-started-btn">Get Started</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section></section>
  </main>
</template>

<script>
import NavBar from "../components/Navbar";
import PostErrands from "../components/PostErrands";

export default {
  components: {
    NavBar,
    PostErrands
  },
  data() {
    return {
      activeItem: "post"
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
#home .hero-section {
  position: relative;
  height: 800px;
  width: 100%;
  background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("../assets/img/mask.png");
  object-fit: contain;
  background-size: 100%;
  background-repeat: no-repeat;
  background-size: cover;
}

#home .hero-section img {
  width: 100%;
  height: 50%;
  object-fit: contain;
}

#home .hero-section .banner {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 8rem;
}

#home .hero-section .jumbotron .lead {
  max-width: 60%;
  margin: 0 auto;
  text-shadow: 1px 3px 6px black;
  font-size: 1.5rem;
}

#home .hero-section .display-4 {
  font-weight: 700;
}

#home .hero-section .start-now {
  color: #13f7ff;
  word-wrap: normal;
  font-weight: bold;
  text-align: start;
  cursor: pointer;
}

#home .hero-section .start-now:hover {
  color: #10d0d6;
}

#home .hero-section .images {
  margin-top: 2rem;
  padding-bottom: 3rem;
}

#home .hero-section .images .mobile-img1 {
  width: 182px;
  height: 43px;
  object-fit: contain;
}

#home .hero-section .images .mobile-img {
  width: 182px;
  height: 63px;
  object-fit: contain;
}

#home .tab-section {
  position: relative;
  display: flex;
  justify-content: center;
}

#home .tab-container {
  width: 65%;
  height: 700px;
  margin: 0 auto;
  box-shadow: 6px -6px 20px #ffffff8f;
  background: #eef6f9;
  border-radius: 15px;
  border: none;
  position: absolute;
  top: -12rem;
}

#home .nav-tabs {
  border: none;
  padding: 23px;
}

#home .nav-tabs .nav-link {
  border: none;
  color: #292929;
  font-weight: 700;
}

#home .nav-tabs .nav-link.active {
  border-bottom: 1px solid #0086b9;
  background: transparent;
  color: #0086b9;
  padding-bottom: 16px;
}

#home .post {
  text-align: center;
}

#home .post h4 {
  color: #292929;
  font-weight: 900;
}

#home .post p {
  width: 53%;
  margin: 0 auto;
  color: #292929;
}

/* FIRST ERRAND SECTION */

.first-post-section {
  background-color: #eef6f9;
  /* margin-top: 30rem; */
}

.intro {
  text-align: left;
}
.section-post-first {
  padding-top: 35rem;
  padding-bottom: 100px;
}
.post-errand-head {
  font-size: 30px;
  font-weight: bold;
  color: #292929;
}

.post-errand-paragraph {
  font-size: 18px;
  line-height: 2rem;
  color: #292929;
}

.inner-heading {
  color: #0086b9 !important;
}

.post-errand-list {
  list-style: none;
  padding-left: 15px;
  line-height: 2rem;
  text-align: left;
}

.post-errand-list li::before {
  content: "\2022";
  color: #0086b9;
  font-weight: 800;
  font-size: 20px;
  display: inline-block;
  width: 1em;
  margin-left: -1em;
}

/* Second Post */
.second-post-section {
  background-color: #eef6f9;
  box-shadow: 0px 2px 2px rgb(31, 30, 30), 0px 0px 15px rgb(231, 230, 230) !important;
  /* box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.24), 0px 0px 15px rgba(0, 0, 0, 0.12); */
  /* height: 26rem; */
}
.section-post-second {
  padding-top: 50px;
  padding-bottom: 70px;
}

.second-block {
  background-color: #e8f4f9;
}

/* Third Post */

.Third-post-section {
  background-color: #eef6f9;
}

.section-post-third {
  padding-top: 90px;
  padding-bottom: 50px;
}

.image-block {
  text-align: center;
}

.btn-apply {
  padding: 0.775rem 0.99rem;
  border-radius: 9px;
}

.post-image {
  height: 30rem;
  margin-top: -80px;
  /* margin-left: 60px; */
}

.post-imagee {
  height: 30rem;
  margin-top: -20px;
}

.wallet-section {
  background-color: #eef6f9;
}

.section-wallet {
  padding-top: 50px;
  padding-bottom: 50px;
}

.wallet-line {
  width: 10%;
  height: 2.5px;
  margin-left: 0;
  margin-right: 0;
  margin-top: 20px;
  background-color: #292929 !important;
  border: 0 none;
}

.wallet-heading {
  margin-left: 20px;
  font-size: 40px;
  color: #0086b9;
  font-weight: 700;
}

.wallet-card {
  text-align: center;
  border: 1px solid transparent;
  margin-top: 30px;
}

.illustration {
  width: rem;
  box-shadow: 0px 2px 2px #1f1e1e, 0px 0px 15px rgb(255, 255, 255);
}

.illustration-box {
  margin: 0 auto;

  /* width: 4rem;
    height: 4rem;  */
  /* padding: 100px; */
}

a,
.app-link {
  color: #0086b9;
  text-decoration: none;
}

a,
.app-link:hover {
  color: #0086b9;
  text-decoration: none;
}

.illustration-box .illustration {
  /* width: 100%; */
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  object-position: center right;
}

.sec-text {
  text-align: center;
  font-size: 15px;
  line-height: 2rem;
  color: #292929;
}

.pri-text {
  font-size: 23px;
  font-weight: 500;
  color: #292929;
  font-weight: 700;
}

.wallet-body {
  flex: 1 1 auto;
  padding: 1.25rem;
}

/* REVIEW SECTION */
.review-section {
  background-color: #eef6f9;
}
.account-reviews {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.get-started-btn {
  margin-left: 8rem;
  padding: 0.5rem 2rem;
  border-radius: 9px;
  background-color: #0086b9;
  color: #fff;
  font-size: 25px;
  font-weight: 800;
  border: #0086b9;
}

.get-started-inside {
  text-align: center;
}

.get-started-btn-block {
  text-align: left;
  padding-top: 0px;
}

.get-started-text {
  color: #292929;
  font-size: 30px;
  font-weight: 800;
  /* margin-right: 40px; */
}

.get-it {
  display: flex;
}

.get-started-outer {
  background-color: rgb(219, 237, 243);
}

.get-started p {
  font-size: 2rem;
}
</style>