<template>
  <main id="wallet">
    <section class="main-container">
      <div class="wallet-card-left">
        <div class="wallet-card__header">
          <div class="total">Total Balance</div>
          <div class="icon">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDropdown"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <img src="@/assets/img/shopping.png" alt />
            </a>

            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">Change wallet Pin</a>
              <a class="dropdown-item" href="#">Withdrawal Notifications</a>
            </div>
          </div>
        </div>
        <div class="amount-section">
          <div class="amount-top">&#8358; 53,300</div>
          <div class="amount-block d-flex">
            <div class="amount-bottom red">&#43;&#8358; 3,000</div>
            <div class="amount-text">escrow</div>
          </div>
        </div>
        <div class="btn-tran d-flex">
          <router-link to="/withdraw" class="btn-withdraw">Withdraw</router-link>
          <router-link to="/fund" class="btn-fund">Fund Wallet</router-link>
          <router-link>
            <button class="btn-withdraw bt-sm apply-now">Withdraw</button>
          </router-link>
          <router-link class="btn-fund bt-sm apply-now">Fund Wallet</router-link>
        </div>
      </div>

      <div class="wallet-card-center">
        <div class="wallet-card__header">
          <div class="total">Income</div>
        </div>
        <div class="amount-section">
          <div class="amount-top">&#43;&#8358; 6,420</div>
        </div>

        <div class="errand-summary">
          <div class="errand-summary-cont d-flex">
            <div class="errand-summary-text">Completed Errands</div>
            <div class="amount-bottom blue">&#43;&#8358; 4,120</div>
          </div>

          <div class="errand-summary-cont1 d-flex">
            <div class="errand-summary-text">Fund Wallet</div>
            <div class="amount-bottom blue">&#43;&#8358; 2,200</div>
          </div>
        </div>
      </div>

      <div class="wallet-card-center">
        <div class="wallet-card__header">
          <div class="total">Expenditure</div>
        </div>
        <div class="amount-section">
          <div class="amount-top">&#8722;&#8358; 3,420</div>
        </div>

        <div class="errand-summary">
          <div class="errand-summary-cont d-flex">
            <div class="errand-summary-text">Send Errands</div>
            <div class="amount-bottom red">&#8722;&#8358; 1,110</div>
          </div>

          <div class="errand-summary-cont1 d-flex">
            <div class="errand-summary-text">Withdrawals</div>
            <div class="amount-bottom red">&#8722;&#8358; 2,200</div>
          </div>
        </div>
      </div>
    </section>

    <section class="section-wallet-tab">
      <div class="wallet-tab-text blue">Wallet Transactions</div>
      <div class="wallet-tab-block">
        <div class="wallet-tab">
          <ul class="nav nav-tabs nav-justified">
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('all')"
                :class="{ active: isActive('all') }"
                href="#all"
              >All</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('credit')"
                :class="{ active: isActive('credit') }"
                href="#credit"
              >Credit</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('debit')"
                :class="{ active: isActive('debit') }"
                href="#debit"
              >Debit</a>
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click.prevent="setActive('escrow')"
                :class="{ active: isActive('escrow') }"
                href="#escrow"
              >Escrow</a>
            </li>
          </ul>
          <div class="tab-content d-flex py-3" id="myTabContent">
            <div class="tab-pane fade" :class="{'active show': isActive('all')}" id="all">
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Was paid for Errand</h4>
                    <div class="detail-amt detail blue">&#43;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Was paid for Errand</h4>
                    <div class="detail-amt detail blue">&#43;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('credit')}" id="credit">
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail blue">&#43;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail blue">&#43;&#8358; 500</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('debit')}" id="debit">
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 50</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 50</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" :class="{'active show': isActive('escrow')}" id="escrow">
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 50</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>Jan.
                      <span>'</span>20
                    </div>
                  </div>
                </div>
              </div>
              <hr />
              <div class="d-flex all">
                <div class="d-flex">
                  <div class="detail-img d-flex">
                    <img src="@/assets/img/outgoing.png" alt="outgoing-card" />
                    <h6 class="user-name">David O</h6>
                  </div>
                  <div class="wallet-details d-flex">
                    <h4 class="detail detail-text">Payment for Errand</h4>
                    <div class="detail-amt detail red">&#8722;&#8358; 50</div>

                    <div class="detail-date detail">
                      12
                      <span>,</span>
                      Jan.
                      <span>'</span>20
                    </div>
                  </div>
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
export default {
  data() {
    return {
      activeItem: "all"
    };
  },

  methods: {
    isActive(menuItem) {
      return this.activeItem === menuItem;
    },

    setActive(menuItem) {
      return (this.activeItem = menuItem);
    }
  }
};
</script>

<style scoped>
#wallet .main-container {
  display: grid;
  grid-template-columns: auto auto auto;
  grid-gap: 2rem;
}

/* WALLET CARD LEFT START  */

#wallet .main-container .wallet-card-left {
  width: 23rem;
  height: 12rem;
  background: #ffffff;
  box-shadow: 0px 3px 6px #00000029;
  padding: 12px;
}

#wallet .main-container .wallet-card__header {
  display: flex;
  justify-content: space-between;
  /* margin-top: 27px; */
}

#wallet .main-container .wallet-card__header .total {
  color: #7a9ba8d8;
  font-size: 14px;
  font-weight: 700;
}

#wallet
  .main-container
  .wallet-card-left
  .wallet-card__header
  .dropdown-toggle::after {
  display: none;
}

#wallet .main-container .wallet-card-left .wallet-card__header .dropdown-menu {
  margin-left: -6.5rem;
}

#wallet
  .main-container
  .wallet-card-left
  .wallet-card__header
  .dropdown-menu
  .dropdown-item {
  font-size: 13px;
}

#wallet .main-container .wallet-card__header .icon img {
  width: 14px;
  height: 14px;
}

#wallet .main-container .amount-section .amount-top {
  font-size: 30px;
  color: #000000;
  font-weight: bold;
}

#wallet .main-container .amount-block {
  margin-left: 17px;
}

#wallet .main-container .amount-block .amount-bottom {
  font-size: 15px;
  font-weight: bold;
}

#wallet .main-container .amount-block .amount-text {
  color: #7a9ba8d8;
  font-size: 12px;
  font-weight: bold;
  margin-top: 3px;
  margin-left: 3px;
}

#wallet .main-container .btn-tran {
  justify-content: space-between;
  margin-top: 2rem;
}

#wallet .main-container .btn-tran .btn-withdraw {
  color: #0086b9;
  background-color: #ffffff;
  border: 1px solid #0086b9;
  font-weight: bold;
  border-radius: 4px;
  padding: 04px;
  text-decoration: none;
}

#wallet .main-container .btn-tran .btn-fund {
  color: #ffffff;
  font-weight: bold;
  background-color: #0086b9;
  border: 1px solid #0086b9;
  border-radius: 4px;
  padding: 04px;
  text-decoration: none;
}

/* WALLET CARD LEFT END  */

/* WALLET CARD CENTER START  */
#wallet .main-container .wallet-card-center {
  width: 17rem;
  height: 12rem;
  background: #ffffff;
  box-shadow: 0px 3px 6px #00000029;
  padding: 12px;
}

#wallet .main-container .errand-summary {
  margin-top: 3.2rem;
}

#wallet .main-container .errand-summary-cont .errand-summary-text {
  color: #7a9ba8d8;
  font-weight: bold;
}

#wallet .main-container .errand-summary-cont .amount-bottom {
  font-weight: bold;
  margin-left: 3px;
}

#wallet .main-container .errand-summary-cont1 .errand-summary-text {
  color: #7a9ba8d8;
  font-weight: bold;
}

#wallet .main-container .errand-summary-cont1 .amount-bottom {
  font-weight: bold;
  margin-left: 3px;
}

.red {
  color: #b80909;
}

.blue {
  color: #0086b9;
}

/* WALLET CARD CENTER END  */

/* WALLET TAB START  */

#wallet .section-wallet-tab {
  margin-top: 2rem;
  background: #ffffff;
  box-shadow: 3px 0px 20px #0000004a;
  height: auto;
}

#wallet .section-wallet-tab .wallet-tab .nav-item .nav-link {
  color: #7a9ba8d8;
  font-weight: bold;
}

#wallet .section-wallet-tab .wallet-tab .nav-item .nav-link.active {
  color: #0086b9;
  font-weight: bold;
}

#wallet .section-wallet-tab .wallet-tab-text {
  font-weight: bold;
  padding: 30px 0px 30px 30px;
}

#wallet .section-wallet-tab .tab-content img {
  width: 35px;
  height: 35px;
  margin-top: -7px;
  object-fit: contain;
}

#wallet .section-wallet-tab .tab-content .user-name {
  color: #000000;
  font-weight: bold;
  margin-left: 4px;
}

#wallet .section-wallet-tab .all .detail {
  margin-left: 09rem;
}

#wallet .section-wallet-tab .all .detail-img {
  margin-left: 3rem;
}

#wallet .section-wallet-tab .all .detail-text {
  font-size: 16px;
  font-weight: bold;
}

#wallet .section-wallet-tab .all .detail-amt {
  font-weight: bold;
}

#wallet .section-wallet-tab .all .detail-date {
  font-size: 16px;
  font-weight: bold;
}

/* #wallet .wallet-tab-block {
  background: #ffffff;
  box-shadow: 3px 0px 20px #0000004a;
  height: auto;
} */

#wallet .wallet-tab {
  /* width: 95%; */
  /* height: auto; */
  /* box-shadow: 3px 0px 20px #0000004a; */
  /* background: #ffffff; */
  /* border-radius: 15px; */
  border: none;
}

.nav-tabs .nav-item.show .nav-link,
.nav-tabs .nav-link.active {
  border: none;
}

/* .nav-tabs .nav-link {
  border: none;
} */

.wallet-details {
  color: #000000;
}

/* WALLET TAB END  */
</style>