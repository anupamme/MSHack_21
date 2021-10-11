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
          <div class="icon-circle icon-circle-org">
            <img src="../../assets/wallet.png" alt="" />
          </div>
          <div>
            <div class="top-head">Wallet Balances</div>
            <div class="amount">$12,786.12</div>
          </div>
        </div>
        <div class="single-card">
          <div class="icon-circle icon-circle-pink">
            <img src="../../assets/stake.png" alt="" />
          </div>
          <div>
            <div class="top-head">Total Staked</div>
            <div class="amount">$12,786.12</div>
          </div>
        </div>
        <div class="single-card">
          <div class="icon-circle icon-circle-green">
            <img src="../../assets/happiness.png" alt="" />
          </div>
          <div>
            <div class="top-head">Total Pending</div>
            <div class="amount">$12,786.12</div>
          </div>
        </div>
      </div>

      <div class="binance-section">
        <div class="flex flex-space-between">
          <div class="coin-head">
            <img src="../../assets/coinIcons/56.png" alt="" /> Binance
          </div>
          <div class="calc">
            $754.12 + $1,185.45 <span style="color: #16a548"> + $13.29 </span>
          </div>
        </div>

        <div class="bottom-cards-main">
          <div class="single-card">
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
      align-items: center;
      margin-top: 60px;
      .single-card {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        height: 60px;
        width: 30%;
        background-color: #0b2025;
        border: 1px solid #37474b;
        border-radius: 2px;
        margin: 0px 10px;
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
          margin-right: 12px;
          border: 1px solid #4a4646;
          border-radius: 50%;
        }
      }
      .calc {
        font-weight: 700;
        font-size: 18px;
      }

      .single-card {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        height: 54px;
        width: 94%;
        background-color: #0b2025;
        border: 1px solid #37474b;
        border-radius: 2px;
        margin: 30px 10px;
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