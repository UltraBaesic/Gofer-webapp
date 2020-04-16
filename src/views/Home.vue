<template>
  <main id="home">
    <section class="hero-section">
      <nav-bar></nav-bar>
       <div class="banner">
          <div class="jumbotron bg-transparent text-white text-center">
            <h1 class="display-4">Get someone to do your tasks for you</h1>
            <p class="lead">Get connected to someone who can run your errands for you while you do your thing. You can run just any type of errand. <span class="start-now"> Start Now</span></p>
            <div class="images">
                <img class="mobile-img1" src="@/assets/img/appstore.png" alt="appstore">
                <img class="mobile-img" src="@/assets/img/playstore.png" alt="appstore">
            </div>
          </div>
      </div>
    </section>
    <section class="tab-section">
      <div class="tab-container">
        <div class="tab-list">
          <ul class="nav nav-tabs nav-justified">
            <li class="nav-item">
              <a class="nav-link" @click.prevent="setActive('post')" :class="{ active: isActive('post') }" href="#post">Post Errands</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" @click.prevent="setActive('run')" :class="{ active: isActive('run') }" href="#run">Run Errands</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" @click.prevent="setActive('get')" :class="{ active: isActive('get') }" href="#get">Get Verified</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" @click.prevent="setActive('join')" :class="{ active: isActive('join') }" href="#join">Join us</a>
            </li>
          </ul>
          <div class="tab-content py-3" id="myTabContent">
            <div class="tab-pane fade" :class="{'active show': isActive('post')}" id="post">
              <div class="d-flex justify-content-center post">
                <div>
                  <h4>What Kind of Errand do you want done?</h4>
                  <p>The type of errand you can post is absolutely limitless, if you can think it you can post. you can get started and start posting, select a category below to start posting</p>
                  <post-errands></post-errands>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('run')}" id="run">
              <div class="d-flex justify-content-center run">
                <div>
                  <h4>You can Run Errands for People</h4>
                  <p>Everybody can run errands, make money by running errands for people. bid for errands around you and earn money on the go, no special skill required to run errands for people. You can pick up just any type of errand</p>
                  <run-errands></run-errands>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('get')}" id="get">
              <div class="d-flex justify-content-center get">
                <div>
                  <h4>Get your Account Verified</h4>
                  <p>Everybody can run errands, make money by running errands for people. bid for errands around you and earn money on the go, no special skill required to run errands for people. You can pick up just any type of errand</p>
                  <get-verified></get-verified>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('join')}" id="join">
              <div class="d-flex justify-content-center join">
                <div>
                  <h4>Apply to Become a Merchant</h4>
                  <p>You want to run our errands for us, come on board and help us help other people run errands while you make money.</p>
                  <join-us></join-us>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="d-flex justify-content-between post-errand-section">
      <div class="col-lg-5 col-md-8 col-sm-12">
       <div class="image-background"></div>
      </div>
    </section>
  </main>
</template>

<script>
import NavBar from '../components/Navbar'
import PostErrands from '../components/PostErrands'
import RunErrands from '../components/RunErrands'
import GetVerified from '../components/GetVerified'
import JoinUs from '../components/JoinUs'

export default {
  components: {
    NavBar,
    PostErrands,
    RunErrands,
    GetVerified,
    JoinUs
  },
  data(){
    return {
      activeItem: 'post'
    }
  },
  methods: {
    isActive(menuItem){
      return this.activeItem === menuItem
    },
    setActive(menuItem){
      this.activeItem = menuItem
    }
  }
}
</script>

<style scoped>

#home .hero-section {
  position: relative;
  height: 800px;
  width: 100%;
  background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('../assets/img/mask.png');
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
  height: auto;
  margin: 0 auto;
  box-shadow: 6px -6px 20px #FFFFFF8F;
  background: #EEF6F9;
  border-radius: 15px;
  border: none;
  margin-top: -228px;
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
  border-bottom: 1px solid #0086B9;
  background: transparent;
  color: #0086B9;
  padding-bottom: 16px;
}

#home .post,
#home .run,
#home .get,
#home .join
{
  text-align: center;
}

#home .post h4,
#home .run h4,
#home .get h4,
#home .join h4
{
  color: #292929;
  font-weight: 900;
}

#home .post p,
#home .run p,
#home .get p,
#home .join p
{
  width: 77%;
  margin: 0 auto;
  font-size: 15px;
  color: #292929;
}

#home .post-errand-section {
  padding: 60px 120px;
}

#home .post-errand-section .image-background {
  position: relative;
}

</style>