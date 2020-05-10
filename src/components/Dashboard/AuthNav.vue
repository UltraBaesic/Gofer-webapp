<template>
  <main id="auth-nav">
    <nav class="nav">
      <div class="d-flex justify-content-between align-items-center logo-container">
        <img src="@/assets/img/auth-logo.png" alt="" class="logo-image">
        <sub class="logo-text">Gofer</sub>
      </div>
      <ul class="list-unstyled d-flex justify-content-between align-items-center mt-2 nav-links">
        <li>
          <router-link to="#" class="active">All Errands</router-link>
        </li>
        <li>
          <router-link to="#">Post Errand</router-link>
        </li>
        <li>
          <router-link to="#">Wallet</router-link>
        </li>
        <li>
          <router-link to="#">Profile</router-link>
        </li>
        <li class="d-flex justify-content-between position-relative">
          <i class="material-icons bell">notifications_none</i>
          <div class="notif-circle"></div>
        </li>
        <li class="dropdown img-drop">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDropdown"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
             <img src="@/assets/img/profile.png" alt="profile-img" class="profile-img">
             <sub class="ml-2"><i class="fas fa-angle-down caret-down"></i></sub>
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">Logout</a>
            </div>
          </li>
      </ul>
    </nav>
  </main>
</template>

<script>
export default {
  
}
</script>

<style scoped>
@import url(https://fonts.googleapis.com/icon?family=Material+Icons);

#auth-nav {
  background: #EEF6F9;
  box-shadow: 0px 3px 22px #0086B930;
  padding: 10px 20px;
}

#auth-nav .nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#auth-nav .nav .logo-container {
  width: 4rem;
  margin-top: -1rem;
}

#auth-nav .nav .logo-container .logo-image{
  width: 48%;
}

#auth-nav .nav .logo-container .logo-text {
  padding-top: 10px;
  color: #0086B9;
  font-size: 20px;
  padding-left: 4px;
  margin-top: -9px;
}

#auth-nav .nav-links li {
  padding: 0px 30px;
}

#auth-nav .nav-links li a {
  color: #7A9BA8D9;
  text-decoration: none;
}

#auth-nav .nav-links li a.active {
  color: #0086B9;
  border-bottom: 2px solid #0086B9;
  display: inline-block;
  line-height: 0.85;
  padding-bottom: 3px;
}

#auth-nav .nav-links .notif {
  color: #6B6B6B;
  margin-top: 5px;
}

#auth-nav .material-icons.bell {
  color: #0086B9;
}
#auth-nav .nav-links .notif-circle {
  position: absolute;
  width: 7px;
  height: 7px;
  border-radius: 100%;
  top: 3px;
  left: 44px;
  background: #DB6314;
}

#auth-nav .profile-img {
  width: 30px;
  height: 30px;
  object-fit: contain;
}

#auth-nav .dropdown-toggle::after {
  display: none;
}

#auth-nav .caret-down {
  font-size: 18px;
}

#auth-nav .img-drop {
  padding: 0 !important;
}

#auth-nav .dropdown-menu {
  margin-left: -4rem;
}

</style>