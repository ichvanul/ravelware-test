<template>
  <div class="color-page">
    <section class="title">
      <h1>Daftar Mobil Sesuai Warna</h1>
    </section>
    <div class="car-color" v-bind:class="{ addexpand: expanding }">
      <section class="color">
        <div class="reg">
          <select name="warna" id="warna" class="warna">
            <option value="1">Hitam</option>
            <option value="2">Merah</option>
            <option value="3">Putih</option>
            <option value="4">Abu-Abu</option>
          </select>
          <div class="orange"><i class="fas fa-plus"></i></div>
        </div>
        <section class="list-color" v-for="item in 10" :key="item.id">
          <div class="info">
            <p>
              No. Polisi: <br />
              B 1234 KB
            </p>
            <p class="data">
              Tipe: <br />
              SUV
            </p>
            <p class="data">
              Tempat Parkir: <br />
              A1
            </p>
            <P class="data"
              >Tanggal & Jam Masuk: <br />
              2020-07-07 07:00</P
            >
            <P class="data"
              >Tanggal & Jam Keluar: <br />
              2020-07-07 12:00</P
            >
          </div>
        </section>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "Color",
  props: ["expanding"]
};
</script>

<style lang="scss" scoped>
.color-page {
  display: none;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .car-color {
    background: white;
    width: 1060px;
    margin-left: 30px;
    margin-bottom: 50px;
    border-radius: 10px;
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
    padding: 20px;
    box-sizing: border-box;
    transition: 0.5s;
    .color {
      display: flex;
      flex-wrap: wrap;
      width: 100%;
      padding: 10px;
      box-sizing: border-box;
      .reg {
        display: flex;
        align-items: center;
        margin-right: 50px;
        .warna {
          height: 30px;
          width: 150px;
          border: 0.5px solid #bababa;
          border-radius: 5px 0 0 5px;
          color: #bababa;
        }
        .orange {
          display: flex;
          align-items: center;
          justify-content: center;
          background: #0066ff;
          height: 30px;
          width: 30px;
          color: #ffffff;
          border-radius: 0 10px 10px 0;
        }
      }
    }
    .list-color {
      display: flex;
      width: 100%;
      height: 60px;
      box-shadow: 0px 5px 9px -2px rgba(0, 0, 0, 0.1);
      padding: 15px;
      box-sizing: border-box;
      margin-bottom: 10px;
      .info {
        display: flex;
        height: 100%;
        justify-content: space-between;
        padding: 3px;
        box-sizing: border-box;
        font-size: 14px;
        .data {
          margin-left: 110px;
        }
        .phone {
          display: flex;
          p {
            font-size: 12px;
          }
          .or {
            color: #0066ff;
            margin-right: 5px;
          }
        }
        .status {
          display: flex;
          p {
            font-size: 12px;
          }
          .vi {
            color: #82bf96;
            margin-right: 5px;
            font-size: 12px;
          }
        }
      }
    }
  }
  .addexpand {
    width: 1290px;
    .list-color {
      .info {
        .data {
          margin-left: 170px;
        }
      }
    }
  }
}

@media only screen and (max-width: 1024px) {
  .color-page {
    display: none;
    flex-direction: column;
    width: 100%;
    background: #f2f3f5;
    .title {
      padding: 15px;
    }
    .car-color {
      background: white;
      width: 700px;
      margin-left: 30px;
      margin-bottom: 50px;
      border-radius: 10px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      padding: 20px;
      box-sizing: border-box;
      transition: 0.5s;
      .color {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        padding: 10px;
        box-sizing: border-box;
        .reg {
          display: flex;
          align-items: center;
          margin-right: 50px;
          .warna {
            height: 30px;
            width: 150px;
            border: 0.5px solid #bababa;
            border-radius: 5px 0 0 5px;
            color: #bababa;
          }
          .orange {
            display: flex;
            align-items: center;
            justify-content: center;
            background: #0066ff;
            height: 30px;
            width: 30px;
            color: #ffffff;
            border-radius: 0 10px 10px 0;
          }
        }
      }
      .list-color {
        display: flex;
        width: 100%;
        height: 100px;
        box-shadow: 0px 5px 9px -2px rgba(0, 0, 0, 0.1);
        padding: 15px;
        box-sizing: border-box;
        margin-bottom: 10px;
        .info {
          display: flex;
          height: 100%;
          justify-content: space-between;
          padding: 3px;
          box-sizing: border-box;
          font-size: 14px;
          .data {
            margin-left: 81px;
          }
          .phone {
            display: flex;
            p {
              font-size: 12px;
            }
            .or {
              color: #0066ff;
              margin-right: 5px;
            }
          }
          .status {
            display: flex;
            p {
              font-size: 12px;
            }
            .vi {
              color: #82bf96;
              margin-right: 5px;
              font-size: 12px;
            }
          }
        }
      }
    }
  }
}
</style>
