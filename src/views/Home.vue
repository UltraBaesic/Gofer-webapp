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
  </main>
</template>

<script>
import NavBar from '../components/Navbar'
import PostErrands from '../components/PostErrands'

export default {
  components: {
    NavBar,
    PostErrands
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
  height: 610px;
  margin: 0 auto;
  box-shadow: 6px -6px 20px #FFFFFF8F;
  background: #EEF6F9;
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
  border-bottom: 1px solid #0086B9;
  background: transparent;
  color: #0086B9;
  padding-bottom: 16px;
}

#home .post{
  text-align: center;
}

#home .post h4{
  color: #292929;
  font-weight: 900;
}

#home .post p{
  width: 53%;
  margin: 0 auto;
  color: #292929;
}
</style>