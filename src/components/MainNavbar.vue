<template>
  <header>
    <nav class="navbar navbar-expand-md navbar-light nav-shadow">
      <a class="navbar-brand ml-5">
        <img src="@/assets/img/logo.png" style="width:110px; margin-top: -14px;" alt="logo" />
      </a>
      <button
        class="navbar-toggler navbar-toggler-right"
        type="button"
        data-toggle="collapse"
        data-target="#navb"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navb">
        <ul class="navbar-nav ml-auto">
          <ul class="navbar-nav position-relative">
            <li class="nav-item">
              <a class="nav-link active" id="all-errands" href="#">All Errands</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" id="post-errand" href>Post Errand</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href>Wallet</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href>Profile</a>
            </li>
          </ul>
        </ul>
        <form class="form-inline my-2 my-lg-0">
          <div class="notification-box my-sm-2">
            <i class="icon-material-outline-notifications"></i>
            <span class="notification">9+</span>
          </div>
          <div class="user-box my-sm-0"></div>
          <li class="nav-item dropdown">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDropdown"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <img src="@/assets/img/idris.jpg" class="profile-picture" alt="profile-pix" />
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">User Action</a>
              <a class="dropdown-item" href="#">Another action</a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="#">Something else here</a>
            </div>
          </li>
        </form>
      </div>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 992px) {
  .navbar-expand-lg .navbar-nav .nav-link {
    padding-left: 1.5rem;
    padding-right: 1.5rem;
  }
}

.nav-link {
  position: relative;
}

.nav-link.active:before {
  position: absolute;
  left: 30%;
  text-align: center;
  width: 50px;
  bottom: 0;
  content: "";
  border-bottom: 2px solid #0086b9;
}

.logo-img {
  width: 110px;
  margin-top: -14px;
}

.icon-material-outline-notifications {
  font-size: 26px;
  color: #0086b9;
}
.navbar {
  background: #eef6f9;
  box-shadow: 0 0.5rem 0.8rem rgba(182, 233, 252, 0.4);
}

.dropdown {
  list-style-type: none;
}

.dropdown-menu {
  left: -8rem;
}

.profile-picture {
  width: 40px;
  height: 40px;
  margin-right: 5px;
  border-radius: 50%;
}

.nav-link.active {
  color: #0086b9 !important;
}

.notification-box {
  position: relative;
  margin-right: 2rem;
  margin-left: 2rem;
  cursor: pointer;
}

.notification {
  height: 16px;
  width: 16px;
  border-radius: 50%;
  background-color: orangered;
  position: absolute;
  top: -3px;
  right: -3px;
  font-size: 8px;
  color: white;
  vertical-align: middle;
  text-align: center;
  line-height: 12px;
  border: 2px solid white;
}
</style>