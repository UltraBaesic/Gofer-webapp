<template>
  <main id="withdraw">
    <ol class="breadcrumb breadcrumb-right-arrow">
      <li class="breadcrumb-item wallet-trans amount-title"></li>

      <li class="breadcrumb-item amount-title back-to-wallet">back to wallet</li>
    </ol>
    <div class="withdraw-header mt-3">Withdraw from your Gofer Account</div>
    <form class="form-container">
      <div class="form-group mt-3">
        <label for class="withdraw-input-text">How much do you want to withdraw</label>
        <input type="text" class="form-control" placeholder="#" />
      </div>
      <div class="form-group">
        <label for class="withdraw-input-text">Choose a Bank</label>
        <input type="text" class="form-control" />
      </div>

      <div class="form-group">
        <label for class="withdraw-input-text">Account Name</label>
        <input type="text" class="form-control" />
      </div>

      <!-- <div class="form-group">
        <label for class="withdraw-input-text">Account Name</label>
        <input type="text" class="form-control" />
      </div>-->

      <div class="form-group">
        <label for class="withdraw-input-text">Account Number</label>
        <input type="password" class="form-control" />
      </div>

      <div class="mb-3 row__container d-flex">
        <div class="form-group">
          <label for class="withdraw-input-text">Your Wallet Pin</label>
          <input type="password" class="form-control pin-wallet" placeholder="0 0 0 0" />
        </div>
        <div class="withdraw-btn-cont">
          <button class="btn btn-sm withdraw-btn">Withdraw</button>
        </div>
      </div>
    </form>
  </main>
</template>

<script>
export default {};
</script>


<style scoped>
#withdraw .breadcrumb {
  background-color: transparent;
  padding: 0;
}

#withdraw .breadcrumb-right-arrow .back-to-wallet {
  color: #0086b9;
  font-weight: bold;
  padding: 0;
}

#withdraw .breadcrumb-right-arrow .breadcrumb-item + .breadcrumb-item::before {
  content: "<";
  vertical-align: top;
  font-size: 30px;
  line-height: 15px;
  color: #0086b9;
  margin-top: 05px;
  font-weight: bold;
}

#withdraw .withdraw-header {
  font-weight: bold;
  color: #000000;
  padding-left: 1rem;
}

#withdraw .form-container {
  padding-left: 1rem;
}

#withdraw .form-container .withdraw-input-text {
  font-weight: 600;
  color: #000000;
}

#withdraw .form-container .withdraw-btn {
  color: #ffffff;
  font-weight: bold;
  background-color: #0086b9;
  border: 1px solid #0086b9;
  border-radius: 4px;
  padding: 6px 10px;
}

/* #widthdraw .withdraw .row__container {
} */

#withdraw .form-container .withdraw-btn-cont {
  margin-top: 2.1rem;
  margin-right: -rem;
}

#withdraw .form-container .pin-wallet {
  width: 50%;
}
</style>