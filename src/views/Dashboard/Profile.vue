<template>
  <main id="profile">
    <section class="main-container">
      <div class="profile-card-left">
        <div class="profile-card__header">
          <div class="profile-img-block">
            <img src="@/assets/img/profile.png" alt class="profile-img" />
          </div>
          <div class="profile-personal-details">
            <div class="profile-name">Steven Peters</div>
            <div class="profile-email">stevenpeters@gmail.com</div>
            <div class="profile-number">08123456789</div>
          </div>
          <div class="dash-stars">
            <i class="material-icons">star</i>
            <i class="material-icons">star</i>
            <i class="material-icons">star</i>
            <i class="material-icons">star_half</i>
            <i class="material-icons">star_border</i>
          </div>

          <button class="btn-edit-profile">Edit Profile</button>
          <!-- <example-modal></example-modal> -->
          <!-- <button class="verify-block" @click="$refs.modal2.open">Show Modal 2</button> -->
          <!-- <div class="modal-content">
              <div class="modal-header">
                  <button type="button" class="close shadow-sm" data-dismiss="modal">&times;</button>
              </div>
              <div>
                  <p class="modal-text text-center font-weight-bold">Edit Profile</p>
              </div>
              <div class="verify-msg text-center p-4">
                <div class="user-picture">
                    <div class="pix-wrapper">
                        <img class="dash-profile" src="@/assets/img/profile.png" alt="">
                        <i class="material-icons verified-logo mr-2">edit</i></div>
                </div>
                <div class="form-group text-left">
                    <label for="" class="text-dark pt-0 pb-0">Name: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="Steven"
                        name="text1"><label for="" class="text-dark pt-0 pb-0">Email: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="steven.peters@gmail.com"
                        name="text1"><label for="" class="text-dark pt-0 pb-0">Phone No: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="08023456789"
                        name="text1">
                </div>
                <div class="mt-3">
                    <a class="btn mt3 btn-lg btn-primary px-5 pointer text-white">Submit</a>
                </div>
              </div>
          </div>-->

          <div class="verify-block d-flex">
            <img src="@/assets/img/shopping.png" alt />
            <div class="verify">Verify Your Account</div>
          </div>
        </div>
      </div>

      <div class="profile-card-center">
        <div class="profile-card__header">
          <div class="detail-header">Notifications</div>

          <div class="detail d-flex" v-for="i in 3" :key="i">
            <img src="@/assets/img/shopping.png" alt />
            <div class="verify-details">
              <div class="errand-notif">You have 2 new Message</div>
              <div class="errand-notif-detail">
                Artsian
                <span>,</span>Cleaning request
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="profile-card-right">
        <div class="profile-card__header">
          <div class="card-right-text">Errand History</div>
        </div>

        <div class="errand-duty-block">
          <div class="d-flex errands-post">
            <div class="errand-duty">You posted</div>
            <p class="date">12, Jan.</p>
          </div>
          <h6>Shopping</h6>
          <p>I work in VI, but i need to wash my car, I need someone to help me wash it ....</p>
        </div>
        <div class="errand-duty-block" v-for="i in 5" :key="i">
          <div class="d-flex errands-post">
            <div class="errand-duty">You completed</div>
            <p class="date">12, Jan.</p>
          </div>
          <h6>Pick-up &#38; Delivery</h6>
          <p>I work in VI, but i need to wash my car, I need someone to help me wash it ....</p>
        </div>
      </div>
    </section>

    <section class="section-review">
      <div class="reviews-block">
        <div class="review-header">Reviews</div>

        <div class="errand-summ d-flex" v-for="i in 5" :key="i">
          <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
          <div class="dash-stars">
            <i class="material-icons">star</i>
            <i class="material-icons">star</i>
            <i class="material-icons">star</i>
            <i class="material-icons">star_half</i>
            <i class="material-icons">star_border</i>

            <h6>David O</h6>
            <p>It was quite interesting having him do my shopping for me, I asked her to help me buy some food stuffs in my house and he did a fantastic job.</p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
#profile {
  padding-top: 10px;
}
#profile .main-container {
  display: grid;
  grid-template-columns: auto auto auto;
  grid-gap: 2rem;
}

/* WALLET CARD LEFT START  */

#profile .main-container .profile-card-left {
  width: 16rem;
  height: 18rem;
  background: #ffffff;
  box-shadow: 0px 3px 6px #00000029;
  padding: 12px;
}

#profile .main-container .profile-card-left .profile-card__header {
  text-align: center;
}

#profile
  .main-container
  .profile-card-left
  .profile-card__header
  .profile-personal-details {
  color: #000000;
  font-weight: bold;
}

#profile
  .main-container
  .profile-card-left
  .profile-card__header
  .dash-stars
  .material-icons {
  color: #efce27;
}

#profile
  .main-container
  .profile-card-left
  .profile-card__header
  .btn-edit-profile {
  color: #ffffff;
  font-weight: bold;
  background-color: #0086b9;
  border: 1px solid #0086b9;
  border-radius: 10px;
  padding: 04px 06px;
  text-decoration: none;
  margin-top: 10px;
}

#profile
  .main-container
  .profile-card-left
  .profile-card__header
  .verify-block
  img {
  width: 14px;
  height: 14px;
  margin-top: 5px;
  margin-right: 2px;
  color: #0086b9 !important;
}

.modal-content {
  width: 40rem;
  /* align-item: center; */
  margin-top: -13rem;
}

.modal-text {
  color: #000000;
  font-weight: 800;
}

.modal-header {
  border: none;
}

.modal-header .close {
  position: absolute;
  right: -1rem;
  top: -1.3rem;
  background-color: white;
  width: 2rem;
  height: 2rem;
  text-align: center;
  line-height: 3px;
  border-radius: 50%;
  margin: 0;
  opacity: 1;
  padding: 0;
}

#profile
  .main-container
  .profile-card-left
  .profile-card__header
  .verify-block {
  color: #0086b9;
  margin-top: 10px;
  margin-left: 2rem;
}

/* END */

/* WALLET CARD CENTER START  */

#profile .main-container .profile-card-center {
  width: 18rem;
  height: 18rem;
  background-color: #ffffff;
  box-shadow: 0px 3px 6px #00000029;
  padding: 12px;
}

#profile
  .main-container
  .profile-card-center
  .profile-card__header
  .detail-header {
  color: #7a9ba8d8;
  font-weight: bold;
  padding-left: 12px;
}

#profile
  .main-container
  .profile-card-center
  .profile-card__header
  .detail
  img {
  width: 15px;
  height: 15px;
}

#profile .main-container .profile-card-center .profile-card__header .detail {
  margin-left: 0.7rem;
  margin-top: 1rem;
}

#profile
  .main-container
  .profile-card-center
  .profile-card__header
  .detail
  .verify-details {
  color: #7a9ba8d8;
  margin-left: 10px;
}

#profile
  .main-container
  .profile-card-center
  .profile-card__header
  .detail
  .verify-details
  .errand-notif {
  color: #000000;
  font-size: 13px;
  font-weight: 700;
}

#profile
  .main-container
  .profile-card-center
  .profile-card__header
  .detail
  .verify-details
  .errand-notif-detail {
  font-size: 11px;
  font-weight: 700;
}

/* END */

/* WALLET CARD RIGHT START  */

#profile .main-container .profile-card-right {
  width: auto;
  height: auto;
  background-color: #ffffff;
  box-shadow: 0px 3px 6px #00000029;
  padding: 12px;
}

#profile
  .main-container
  .profile-card-right
  .profile-card__header
  .card-right-text {
  color: #7a9ba8d8;
  font-weight: bold;
  padding: 0px 0 17px 10px;
}

#profile .main-container .profile-card-right .errand-duty-block {
  padding-left: 15px;
}
#profile .main-container .profile-card-right .errand-duty-block .errand-duty {
  color: #0086b9;
  font-size: 12px;
  font-weight: 700;
}

#profile .main-container .profile-card-right .errand-duty-block h6 {
  color: #000000;
  font-weight: 700;
  font-size: 14px;
  margin-bottom: 0;
  margin-top: -10px;
}

#profile .main-container .profile-card-right .errand-duty-block p {
  font-size: 12px;
  color: #2f3131d8;
  margin-top: 05px;
}

#profile .main-container .profile-card-right .errand-duty-block .errands-post {
  justify-content: space-between;
}

#profile
  .main-container
  .profile-card-right
  .errand-duty-block
  .errands-post
  p {
  color: #7a9ba8d8;
  font-size: 11px;
  margin-top: 0px;
}

/* END */

#profile .section-review {
  margin-top: -20rem;
  width: 36rem;
  background: #ffffff;
  box-shadow: 3px 0px 20px #0000004a;
  height: auto;
}

#profile .section-review .reviews-block .review-header {
  color: #7a9ba8d8;
  font-weight: bold;
  padding: 25px 0 20px 25px;
}

#profile .section-review .reviews-block .errand-summ {
  padding-left: 29px;
}

#profile .section-review .reviews-block .dash-stars {
  margin-left: 8px;
}

#profile .section-review .reviews-block img {
  width: 3rem;
  height: 3rem;
  margin-top: 20px;
}

#profile .section-review .reviews-block .dash-stars .material-icons {
  color: #efce27;
}

#profile .section-review .reviews-block .dash-stars h6 {
  color: #000000;
  font-weight: 700;
}

#profile .section-review .reviews-block .dash-stars p {
  color: #2f3131d8;
  font-size: 14px;
  width: 30rem;
  line-height: 25px;
}
</style>