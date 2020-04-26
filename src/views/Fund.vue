<template>
  <main id="fund">
    <ol class="breadcrumb breadcrumb-right-arrow">
      <li class="breadcrumb-item wallet-trans amount-title"></li>

      <li class="breadcrumb-item amount-title back-to-wallet">back to wallet</li>
    </ol>

    <div class="fund-header mt-4">Fund your Wallet</div>
    <div class="img-cont mt-4">
      <div class="choose-card">Pick Card Type</div>
      <ul class="fund-list">
        <li class="fund-item">
          <input type="checkbox" id="myCheckbox1" />
          <label for="myCheckbox1" class="label-input">
            <img src="@/assets/img/verve-logo.png" class="fund-img" />
          </label>
        </li>
        <li class="fund-item">
          <input type="checkbox" id="myCheckbox2" />
          <label for="myCheckbox2" class="label-input">
            <img src="@/assets/img/visa-logo.png" class="fund-img" />
          </label>
        </li>
        <li class="fund-item">
          <input type="checkbox" id="myCheckbox3" />
          <label for="myCheckbox3" class="label-input">
            <img src="@/assets/img/master-card.png" class="fund-img" />
          </label>
        </li>
      </ul>
    </div>
    <form class="form-container">
      <div class="form-group mt-3">
        <label for class="fund-input-text">Card Holders Name</label>
        <input type="text" class="form-control" />
      </div>
      <div class="form-group">
        <label for class="fund-input-text">Card Number</label>
        <input type="text" class="form-control" />
      </div>

      <div class="mb-3 row__container d-flex">
        <div class="form-group">
          <label for class="fund-input-text">Expiry Date</label>
          <input type="password" class="form-control pin-wallet" />
        </div>
        <div class="form-group">
          <label for class="fund-input-text">CVV</label>
          <input type="password" class="form-control pin-wallet" />
        </div>
      </div>

      <div class="form-group form-check mt-4">
        <input type="checkbox" class="form-check-input" id="exampleCheck2" />
        <label
          class="form-check-label fund-input-text"
          for="exampleCheck1"
        >Save details for future Transaction</label>
      </div>

      <div class="fund-btn-cont">
        <button class="btn btn-md fund-btn">Withdraw</button>
      </div>
    </form>
  </main>
</template>

<script>
export default {};
</script>


<style scoped>
#fund .breadcrumb {
  background-color: transparent;
  padding: 0;
}

#fund .breadcrumb-right-arrow .back-to-wallet {
  color: #0086b9;
  font-weight: bold;
  padding: 0;
}

#fund .breadcrumb-right-arrow .breadcrumb-item + .breadcrumb-item::before {
  content: "<";
  vertical-align: top;
  font-size: 30px;
  line-height: 15px;
  color: #0086b9;
  margin-top: 05px;
  font-weight: bold;
}

#fund .fund-header {
  font-weight: bold;
  color: #000000;
  padding-left: 1rem;
}

#fund .img-cont .choose-card {
  font-weight: 600;
  color: #000000;
  padding-left: 1rem;
}

#fund .img-cont .fund-list {
  list-style-type: none;
  padding-left: 0.5rem;
}

#fund .img-cont .fund-list .fund-item {
  display: inline-block;
}

input[type="checkbox"][id^="myCheckbox"] {
  display: none;
  color: #c5eaf8;
}

#fund .img-cont .fund-list .fund-item label {
  border: 1px solid #c5eaf8;
  padding: 05px;
  display: block;
  position: relative;
  margin: 05px;
  cursor: pointer;
}

#fund .img-cont .fund-list .fund-item label:before {
  background-color: white;
  color: white;
  content: " ";
  display: block;
  border-radius: 50%;
  border: 1px solid grey;
  position: absolute;
  top: -5px;
  left: -5px;
  width: 25px;
  height: 25px;
  text-align: center;
  line-height: 28px;
  transition-duration: 0.4s;
  transform: scale(0);
}

#fund .img-cont .fund-list .fund-item label img {
  width: 3rem;
  height: 1rem;
  transition-duration: 0.2s;
  transform-origin: 50% 50%;
}

#fund .img-cont .fund-list .fund-item :checked + .label-input {
  border-color: #c5eaf8;
}

#fund .img-cont .fund-list .fund-item :checked + .label-input:before {
  content: "✓";
  background-color: #0086b9;
  transform: scale(1);
}

#fund .img-cont .fund-list .fund-item :checked + .label-input img {
  transform: scale(0.9);
  /* box-shadow: 0 0 5px #333; */
  z-index: -1;
}

#fund .form-container {
  padding: 1rem;
}

#fund .form-container .fund-input-text {
  font-weight: 600;
  color: #000000;
}

#fund .form-container .fund-btn {
  color: #ffffff;
  font-weight: bold;
  background-color: #0086b9;
  border: 1px solid #0086b9;
  border-radius: 4px;
  padding: 6px 10px;
}

#fund .form-container .fund-btn-cont {
  margin-top: 2.1rem;
  margin-right: -rem;
}

#fund .form-container .pin-wallet {
  width: 60%;
}

#fund .img-cont .platform-card-img .verve-img,
.visa-img,
.master-img {
  width: 3rem;
  height: 1rem;
}
</style>