<template>
  <div class="container">
    <div class="title">
      <h1>Dashboard</h1>
    </div>
    <section class="data-1">
      <div class="card-ppl" v-bind:class="{ stretcy: isStretch }">
        <div class="nomine">
          <section class="count">
            <h5>KEDATANGAN</h5>
            <H2 class="cn-1">2.500</H2>
          </section>
          <section class="icon">
            <img
              src="../../assets/img/fds.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl" v-bind:class="{ stretcy: isStretch }">
        <div class="nomine">
          <section class="count">
            <h5>MEMBER LAMA</h5>
            <H2 class="cn-2">2.000</H2>
          </section>
          <section class="icon">
            <img
              src="../../assets/img/refresh.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="grn"><b>+20%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl " v-bind:class="{ stretcy: isStretch }">
        <div class="nomine">
          <section class="count">
            <h5>MEMBER BARU</h5>
            <H2 class="cn-3">500</H2>
          </section>
          <section class="icon">
            <img
              src="../../assets/img/plus.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="red"><b>-5%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl" v-bind:class="{ stretcy: isStretch }">
        <div class="nomine">
          <section class="count">
            <h5>KELUAR</h5>
            <H2 class="cn-4">1.500</H2>
          </section>
          <section class="icon">
            <img
              src="../../assets/img/exit.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="red"><b>-15%</b> dari minggu lalu</p>
        </div>
      </div>
    </section>
    <section class="data-2">
      <div class="card-data" v-bind:class="{ puck: isPuck }">
        <h4>TOTAL PEMASUKAN</h4>
        <section class="income">
          <h1>RP. 1.500.000</h1>
          <p class="grn"><b>+30%</b> dari bulan lalu</p>
        </section>
        <section class="cart">
          <column-chart
            height="100%"
            :data="income"
            :colors="blue"
          ></column-chart>
        </section>
        <div class="footer">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data" v-bind:class="{ puck: isPuck }">
        <h4>MEMBERSHIP</h4>
        <section class="income">
          <h1>1.200</h1>
          <p class="red"><b>-10%</b> dari bulan lalu</p>
        </section>
        <section class="cart">
          <column-chart
            height="100%"
            width="100%"
            :data="membership"
            :colors="blue"
          ></column-chart>
        </section>
        <div class="footer">
          <p class="red"><b>-10%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data" v-bind:class="{ puck: isPuck }">
        <h4>METODE PEMBAYARAN</h4>
        <section class="cart">
          <pie-chart
            height="100%"
            width="100%"
            :legend="legend"
            :donut="true"
            :data="payment"
            :colors="payColor"
          ></pie-chart>
        </section>
        <div class="footer-2">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data" v-bind:class="{ puck: isPuck }">
        <h4>TRAFIK BERDASARKAN WARNA MOBIL</h4>
        <section class="cart">
          <pie-chart
            height="100%"
            width="100%"
            legend="left"
            :data="traffic"
            :colors="payColor"
          ></pie-chart>
        </section>
        <div class="footer-2">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Dashboard",
  props: ["isStretch", "isPuck"],
  data() {
    return {
      income: {
        JAN: 375,
        FEB: 800,
        MAR: 1200,
        APR: 1125,
        MEI: 800,
        JUN: 1400,
        JUL: 500,
        AGU: 1150,
        SEP: 350,
        OKT: 780,
        NOV: 1000,
        DES: 1600
      },
      membership: {
        JAN: 300,
        FEB: 800,
        MAR: 1000,
        APR: 900,
        MEI: 800,
        JUN: 1100,
        JUL: 400,
        AGU: 500,
        SEP: 800,
        OKT: 950,
        NOV: 1000,
        DES: 800
      },
      traffic: {
        Merah: "10%",
        Putih: "25%",
        Hitam: "55%",
        Lainnya: "10%"
      },
      payment: {
        CASH: 800,
        EMONEY: 800,
        MEMBERSHIP: 600
      },
      payColor: ["#ff3300", "#f2f2f2", "#000000", "#F3C249"],
      blue: ["#5FA2F3"],
      legend: "left"
    };
  }
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .data-1 {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    .card-ppl {
      width: 240px;
      height: 150px;
      background: #ffffff;
      border-radius: 10px;
      margin: 30px 0 0 30px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      box-sizing: border-box;
      overflow: hidden;
      transition: 0.2s all;
      .nomine {
        padding: 10px;
        display: flex;
        .count {
          width: 60%;
          h5 {
            margin-bottom: 15px;
          }
          .cn-1 {
            font-size: 30px;
            color: #82bf96;
          }
          .cn-2 {
            font-size: 30px;
            color: #924a9f;
          }
          .cn-3 {
            font-size: 30px;
            color: #5993dd;
          }
          .cn-4 {
            font-size: 30px;
            color: #d2353f;
          }
        }
      }
      .footer {
        height: 30px;
        width: 100%;
        background: #fcf3db;
        padding: 5px;
        .grn {
          font-size: 12px;
          color: #82bf96;
        }
        .red {
          font-size: 12px;
          color: #d2353f;
        }
      }
    }
    .stretcy {
      width: 300px !important;
    }
  }
  .data-2 {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    margin-bottom: 50px;
    .card-data {
      padding: 10px;
      box-sizing: border-box;
      width: 510px;
      height: 300px;
      background: #ffffff;
      border-radius: 10px;
      margin: 30px 0 0 30px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      transition: 0.5s all;
      h4 {
        display: flex;
        width: 100%;
        margin-bottom: 30px;
      }
      .income {
        width: 100%;
        display: flex;
        justify-content: space-between;
        margin-bottom: 5px;
        .grn {
          font-size: 13px;
          color: #82bf96;
        }
        .red {
          font-size: 13px;
          color: #d2353f;
        }
      }
      .cart {
        width: 100%;
        height: 200px;
        box-sizing: border-box;
        padding: 2px;
      }
      .footer {
        display: none;
        .grn {
          font-size: 12px;
          color: #82bf96;
        }
        .red {
          font-size: 12px;
          color: #d2353f;
        }
      }
      .footer-2 {
        display: none;
      }
    }
    .puck {
      width: 630px;
    }
  }
}
@media only screen and (max-width: 600px) {
  .container {
    align-items: center;
    .data-1 {
      justify-content: center;
      .card-ppl {
        width: 300px !important;
        .footer {
          display: flex;
          justify-content: center;
        }
      }
    }
    .data-2 {
      justify-content: center;
      .card-data {
        width: 300px !important;
        height: 210px;
        padding: 10px 0 0 0;
        box-sizing: border-box;
        overflow: hidden;
        h4 {
          justify-content: center;
          margin-bottom: 0;
          font-size: 12px;
        }
        .income {
          h1 {
            margin: 0;
          }
          justify-content: center;
          .grn {
            display: none;
          }
          .red {
            display: none;
          }
        }
        .cart {
          height: 120px;
          margin-top: 10px;
        }
        .footer {
          display: flex;
          width: 100%;
          justify-content: center;
          margin-top: 5px;
        }
        .footer-2 {
          display: flex;
          align-items: center;
          background: #fcf3db;
          height: 30px;
          width: 100%;
          justify-content: center;
          margin-top: 25px;
          .grn {
            font-size: 13px;
            color: #82bf96;
          }
          .red {
            font-size: 13px;
            color: #d2353f;
          }
        }
      }
    }
  }
}
</style>
