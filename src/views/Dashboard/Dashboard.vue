<template>
  <div class="Dashboard">
    <TopNav />
    <div class="dashboard-inner">
      <div class="first-sec">
        <div class="flex">
          <p class="side-head">Dashboard</p>
          <div class="ml-20 second-head">15 hours ago</div>
        </div>
        <div class="flex">
          <div class="mr-10 firstDD">
            <el-select v-model="currency" placeholder="Currency">
              <el-option
                class="customDD"
                v-for="(item, index) in currencyList"
                :key="index"
                :label="item.currencyName"
                :value="item.currencyName"
              >
                {{ item.currencyName }}
              </el-option>
            </el-select>
          </div>
          <div class="firstDD secondDD">
            <el-select v-model="value" placeholder="Select">
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value"
              >
              </el-option>
            </el-select>
          </div>
        </div>
      </div>
    </div>

    <div class="dashboard-body">
      <div class="graph">
        <div>
          <div class="top-head">Net Worth</div>
          <div class="amount">$12,786.12</div>
        </div>
      </div>
      <div class="three-cards">
        <div class="single-card">
          <div class="inner main-card" @click="valletBalance = !valletBalance">
            <div class="icon-circle icon-circle-org">
              <img src="../../assets/wallet.png" alt="" />
            </div>
            <div>
              <div class="top-head">Wallet Balances</div>
              <div class="amount">$12,786.12</div>
            </div>
          </div>
          <div class="details-sec" v-if="valletBalance">
            <div class="sep-coin-sec">
              <div class="inner main">
                <div class="flex head">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/ether.png"
                    alt=""
                  />
                  Ethereum
                </div>
                <div class="amt">$9668.54</div>
              </div>

              <div class="inner sub">
                <div class="flex">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/uni_F984.webp"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="head">Uni</div>
                    <div class="sub-head">400.0</div>
                  </div>
                </div>
                <div class="text-right">
                  <div class="head">$9668.54</div>
                  <div class="sub-head">1 uni = $24.06</div>
                </div>
              </div>

              <div class="inner sub">
                <div class="flex">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/ether.png"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="head">Eth</div>
                    <div class="sub-head">400.0</div>
                  </div>
                </div>
                <div class="text-right">
                  <div class="head">$9668.54</div>
                  <div class="sub-head">1 uni = $24.06</div>
                </div>
              </div>
            </div>

            <div class="sep-coin-sec">
              <div class="inner main">
                <div class="flex head">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/ether.png"
                    alt=""
                  />
                  Ethereum
                </div>
                <div class="amt">$9668.54</div>
              </div>

              <div class="inner sub">
                <div class="flex">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/uni_F984.webp"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="head">Uni</div>
                    <div class="sub-head">400.0</div>
                  </div>
                </div>
                <div class="text-right">
                  <div class="head">$9668.54</div>
                  <div class="sub-head">1 uni = $24.06</div>
                </div>
              </div>

              <div class="inner sub">
                <div class="flex">
                  <img
                    class="detail-imgs"
                    src="../../assets/coinIcons/ether.png"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="head">Eth</div>
                    <div class="sub-head">400.0</div>
                  </div>
                </div>
                <div class="text-right">
                  <div class="head">$9668.54</div>
                  <div class="sub-head">1 uni = $24.06</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="single-card">
          <div class="inner main-card">
            <div class="icon-circle icon-circle-pink">
              <img src="../../assets/stake.png" alt="" />
            </div>
            <div>
              <div class="top-head">Total Staked</div>
              <div class="amount">$12,786.12</div>
            </div>
          </div>
        </div>
        <div class="single-card">
          <div class="inner main-card">
            <div class="icon-circle icon-circle-green">
              <img src="../../assets/happiness.png" alt="" />
            </div>
            <div>
              <div class="top-head">Total Pending</div>
              <div class="amount">$12,786.12</div>
            </div>
          </div>
        </div>
      </div>

      <div class="binance-section">
        <div class="bottom-cards-main">
          <div>
            <div class="flex flex-space-between">
              <div class="coin-head">
                <img src="../../assets/coinIcons/56.png" alt="" /> Binance
              </div>
              <div class="calc">
                $754.12 + $1,185.45
                <span style="color: #16a548"> + $13.29 </span>
              </div>
            </div>

            <div class="single-card">
              <div class="inner-sec">
                <div class="flex">
                  <img
                    class="icon"
                    src="../../assets/coinIcons/bvaults.png"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="top-head">bVaults</div>
                    <div class="botm-head">1 pools</div>
                  </div>
                </div>
                <div>
                  <div class="top-head">$785.62</div>
                  <div class="amount">+ $0.44</div>
                </div>
              </div>
              <div class="bin-details-sec">
                <div class="flex-space-between">
                  <div class="flex">
                    <img
                      class="icon"
                      src="../../assets/coinIcons/bdov2_6A12-busd_7D56.webp"
                      alt=""
                    />
                    <div class="text-left">
                      <div class="top-head">BDOV2-BUSD</div>
                      <div class="botm-head">137% / Daily 0.09%</div>
                    </div>
                  </div>

                  <div class="right-sec flex">
                    <div class="divider flex-space-between-only align-start">
                      <div class="text-right mr-20">
                        <div class="botm-head">Risk</div>
                        <div class="top-head">~1.5/5</div>
                      </div>

                      <div class="text-right">
                        <div class="botm-head">Pending</div>
                        <div class="top-head" style="color: #7eae61">$0.40</div>
                        <div class="top-head" style="color: #7eae61">$0.08</div>
                      </div>
                    </div>

                    <div class="divider flex-space-between-only align-start">
                      <div class="text-right mr-20">
                        <div class="botm-head">Yield</div>
                        <div class="top-head" style="color: #7eae61">
                          $49.83
                        </div>
                        <div class="botm-head">165.17649</div>
                      </div>

                      <div class="text-right">
                        <div class="botm-head">Deposit</div>
                        <div class="top-head">$733.90</div>
                        <div class="botm-head">2,432.95863</div>
                      </div>
                    </div>

                    <div class="divider flex-space-between-only align-start">
                      <div class="text-right mr-20">
                        <div class="botm-head">Total</div>
                        <div class="top-head">$783.72</div>
                        <div class="botm-head">165.17649</div>
                      </div>

                      <div class="text-right">


                        <div class="botm-head">Start Date</div>
                        <div class="botm-head">4 months<br> ago</div>
                        <div class="botm-head" style="color: #7eae61">+6.85%</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="single-card">
              <div class="inner-sec">
                <div class="flex">
                  <img
                    class="icon"
                    src="../../assets/coinIcons/autofarm.png"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="top-head">Autofarm</div>
                    <div class="botm-head">1 pools</div>
                  </div>
                </div>
                <div>
                  <div class="top-head">$785.62</div>
                  <div class="amount">+ $0.44</div>
                </div>
              </div>
            </div>
          </div>

          <div>
            <div class="flex flex-space-between mt-75">
              <div class="coin-head">
                <img src="../../assets/coinIcons/137.png" alt="" /> Polygon
              </div>
              <div class="calc">
                $754.12 + $1,185.45
                <span style="color: #16a548"> + $13.29 </span>
              </div>
            </div>

            <div class="single-card">
              <div class="inner-sec">
                <div class="flex">
                  <img
                    class="icon"
                    src="../../assets/coinIcons/eleven.png"
                    alt=""
                  />
                  <div class="text-left">
                    <div class="top-head">Eleven</div>
                    <div class="botm-head">1 pools</div>
                  </div>
                </div>
                <div>
                  <div class="top-head">$785.62</div>
                  <div class="amount">+ $0.44</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import TopNav from "@/components/top-nav/top-nav.vue";
export default {
  name: "Dashboard",
  components: {
    TopNav,
  },
  data() {
    return {
      options: [
        {
          value: "Option1",
          label: "Option1",
        },
        {
          value: "Option2",
          label: "Option2",
        },
        {
          value: "Option3",
          label: "Option3",
        },
        {
          value: "Option4",
          label: "Option4",
        },
        {
          value: "Option5",
          label: "Option5",
        },
      ],
      value: "",
      currency: "USD - $",
      valletBalance: true,
      currencyList: [
        { currencyName: "USD - $" },
        { currencyName: "EUR - €" },
        { currencyName: "AED - د.إ.‏" },
        { currencyName: "AUD - $" },
        { currencyName: "CNY - CN¥" },
        { currencyName: "GBP - £" },
        { currencyName: "IDR - Rp" },
        { currencyName: "INR - টকা" },
        { currencyName: "JPY - ￥" },
        { currencyName: "SAR - ر.س.‏" },
      ],
    };
  },
  methods: {
    // showDetails(cardName){
    // }
  },
};
</script>
<style lang="scss" scoped>
.Dashboard {
  .dashboard-inner {
    .first-sec {
      background-image: linear-gradient(260deg, #071619, #1514148c),
        url("../../assets/background1.png");
      height: 100px;
      background-repeat: no-repeat;
      background-size: cover;
      background-position: 100% 0;
      border: 1px solid #153b44;
      padding: 0 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .side-head {
        font-size: 24px;
        color: #ffffffde;
        font-weight: 500;
      }
      .second-head {
        color: #6c757d !important;
      }
    }
  }
  .dashboard-body {
    padding: 50px 75px;
    .graph {
      .top-head {
        font-size: 17px;
        color: #79898d;
      }
      .amount {
        font-size: 2.4rem;
        font-weight: bold;
      }
    }
    .three-cards {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-top: 60px;
      .main-card {
        cursor: pointer;
      }
      .single-card {
        padding: 20px;
        min-height: 60px;
        width: 30%;
        background-color: #0b2025;
        border: 1px solid #37474b;
        border-radius: 2px;
        margin: 0px 10px;
        .inner {
          display: flex;
          justify-content: space-between;
          align-items: center;
        }
        .icon-circle {
          padding: 10px;
          border-radius: 50%;
          height: 25px;
          width: 25px;
          img {
            width: 25px;
          }
        }
        .icon-circle-org {
          background: #f6a10840;
        }
        .icon-circle-pink {
          background: #e1828240;
          img {
            width: 32px;
            position: relative;
            right: 5px;
            bottom: 4px;
          }
        }
        .icon-circle-green {
          background: #7ef90b26;
        }
        .top-head {
          font-size: 17px;
          color: #79898d;
        }
        .amount {
          font-size: 2rem;
          font-weight: bold;
        }
        .details-sec {
          margin-top: 20px;
          height: 200px;
          overflow-y: auto;
          .sep-coin-sec {
            margin-top: 20px;
            border-bottom: 1px solid gray;
          }
          .detail-imgs {
            width: 23px;
            margin-right: 10px;
          }
          .inner {
            padding: 10px 0;
            padding-right: 10px;
          }
          .main {
            .head {
              color: #5777e7;
            }
            .amt {
              font-size: 18px;
              font-weight: 800;
            }
          }
          .sub {
            .head {
              text-transform: uppercase;
              font-size: 16px;
            }
            .sub-head {
              font-size: 14px;
              color: #79898d;
            }
          }
        }
      }
    }
    .binance-section {
      margin-top: 80px;
      .coin-head {
        font-size: 18px;
        font-weight: 700;
        display: flex;
        align-items: center;
        color: #f4ae14;
        img {
          width: 30px;
          margin: 0 12px;
          border: 1px solid #4a4646;
          border-radius: 50%;
        }
      }
      .calc {
        font-weight: 700;
        font-size: 18px;
      }
      .single-card {
        padding: 20px;
        min-height: 54px;
        width: 94%;
        background-color: #0b2025;
        border: 1px solid #37474b;
        border-radius: 2px;
        margin: 30px 10px;
        .inner-sec {
          display: flex;
          justify-content: space-between;
          align-items: center;
        }
        .icon {
          width: 40px;
          margin-right: 12px;
        }
        .top-head {
          font-weight: 700;
          font-size: 18px;
        }
        .botm-head {
          font-size: 15px;
          color: #79898d;
        }
        .amount {
          font-weight: 700;
          font-size: 18px;
          color: #16a548;
        }
        .bin-details-sec {
          height: 100px;
          padding: 30px 15px;
          border: 1px solid #37474b;
          margin-top: 25px;
          background-color: #10292f;
          .divider {
            border-right: 1px solid;
            padding: 0px 25px;
          }
        }
      }
    }
  }
}
</style>
<style lang="scss">
.Dashboard {
  .dashboard-inner {
    .first-sec {
      .firstDD {
        .el-input__inner {
          background-color: transparent;
          border: 1px solid transparent;
          width: 110px;
          font-size: 16px;
          color: #ffff;
        }
      }
      .secondDD {
        .el-input__inner {
          border: 1px solid #153b44;
          width: 180px;
        }
      }
    }
  }
}
.el-popper .popper__arrow {
  display: none !important;
}
.el-select-dropdown__item.selected,
.el-select-dropdown__item.hover,
.el-select-dropdown__item:hover {
  background-color: #0b2025;
  color: #eb9472;
}
.el-select-dropdown__item {
  font-size: 18px;
  padding: 10px 20px;
  border-bottom: 1px solid #313839;
  background: #0b2025;
  height: auto;
  line-height: auto;
}
.el-select-dropdown__list {
  padding: 0px 0;
}
.el-select-dropdown {
  border: 1px solid #313839;
  border-radius: 0;
}
</style>