<template>
  <div class="gaskir-page">
    <section class="title">
      <h1>Tambah Petugas Parkir</h1>
    </section>
    <section class="main-menu">
      <aside class="list-gas" v-bind:class="{ listretch: stretching }">
        <h3>Daftar Petugas Parkir</h3>
        <section class="contact" v-for="item in 6" :key="item.id">
          <img
            src="../../assets/img/isyana-selfie-6cd5c6baab996bb8e7b791d6b3458033.jpg"
            alt="Petugas"
          />
          <div class="info">
            <p>Isyana</p>
            <div class="phone">
              <i class="fas fa-mobile-alt or"></i>
              <p>+6281245383209</p>
            </div>
            <div class="status">
              <i class="fas fa-check-circle vi"></i>
              <p>Aktif</p>
            </div>
          </div>
        </section>
      </aside>
      <div class="add-gas" v-bind:class="{ addstretch: stretced }">
        <h3>Unggah Dokumen Data Diri</h3>
        <section class="upload">
          <div class="ktp">
            <section class="temp">
              <img src="../../assets/img/upload.svg" alt="upload" />
            </section>
            <button>UNGGAH KTP</button>
            <p>
              Ekstensi File Yang Di Perbolehkan :
              <b>.JPG .JPEG .PNG</b>
            </p>
          </div>
          <div class="ktp">
            <section class="temp">
              <img src="../../assets/img/upload.svg" alt="upload" />
            </section>
            <button>UNGGAH FOTO FIRI</button>
            <p>
              Ekstensi File Yang Di Perbolehkan :
              <b>.JPG .JPEG .PNG</b>
            </p>
          </div>
        </section>
        <h3>Informasi Petugas Parkir</h3>
        <section class="form">
          <div class="form-group">
            <label for="Nama">Nama Petugas Parkir</label>
            <input type="text" id="Nama" />
          </div>
          <div class="form-group">
            <label for="user">Username</label>
            <input type="text" id="user" />
          </div>
          <div class="form-group">
            <label for="nik">NIK</label>
            <input type="text" id="nik" />
          </div>
          <div class="form-group">
            <label for="pasword">Password</label>
            <input type="text" id="pasword" />
          </div>
          <div class="form-group">
            <label for="no">No. Telepon</label>
            <input type="text" id="no" />
          </div>
          <div class="check">
            <p class="active unactive">Aktif</p>
            <checkBox />
          </div>
        </section>
        <footer>
          <div class="button-group">
            <button class="cancel">BATAL</button>
            <button class="save">SIMPAN</button>
          </div>
        </footer>
      </div>
    </section>
  </div>
</template>

<script>
import checkBox from "../module_/checkbox.vue";
export default {
  name: "Gaskir",
  props: ["stretching", "stretced"],
  components: {
    checkBox
  }
};
</script>

<style lang="scss" scoped>
.gaskir-page {
  display: none;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .main-menu {
    display: flex;
    width: 100%;
    margin-bottom: 50px;
    padding: 20px;
    box-sizing: border-box;
    .list-gas {
      width: 300px;
      background: white;
      border-radius: 10px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      padding: 15px;
      transition: 0.5s;
      h3 {
        margin-bottom: 10px;
      }
      .contact {
        display: flex;
        width: 100%;
        height: 100px;
        box-shadow: 0px 5px 9px -2px rgba(0, 0, 0, 0.3);
        padding: 15px;
        box-sizing: border-box;
        margin-bottom: 10px;
        img {
          width: 70px;
          height: 70px;
          border-radius: 50%;
          margin-right: 5px;
        }
        .info {
          display: flex;
          height: 100%;
          flex-direction: column;
          justify-content: space-between;
          padding: 3px;
          box-sizing: border-box;
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
    .listretch {
      width: 400px;
    }
    .add-gas {
      width: 700px;
      background: white;
      margin-left: 30px;
      border-radius: 10px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      padding: 20px;
      box-sizing: border-box;
      transition: 0.5s;
      h3 {
        margin-bottom: 10px;
      }
      .upload {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        margin-bottom: 10px;
        .ktp {
          display: flex;
          flex-direction: column;
          align-items: center;
          width: 280px;
          border: 1px solid #c7c2c2;
          border-radius: 8px;
          padding: 20px;
          box-sizing: border-box;
          margin-top: 10px;
          .temp {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 220px;
            height: 200px;
            box-shadow: 0px 5px 9px -2px rgba(0, 0, 0, 0.3);
            border-radius: 8px;
            margin-bottom: 25px;
            img {
              width: 120px;
              height: 120px;
            }
          }
          button {
            color: #ffffff;
            background: #0066ff;
            border-radius: 5px;
            padding: 5px;
            border: none;
            margin-bottom: 20px;
          }
          p {
            font-size: 10px;
          }
        }
      }
      .form {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        border: #c7c2c2 1px solid;
        border-radius: 10px;
        padding: 10px;
        box-sizing: border-box;
        .form-group {
          display: flex;
          flex-direction: column;
          margin: 0 8px;
          input {
            border: 1px solid #c7c2c2;
            border-radius: 5px;
            width: 300px;
            height: 35px;
            margin: 5px 0;
          }
        }
        .check {
          display: flex;
          flex-direction: column;
          margin: 0 8px;
          .active {
            margin-bottom: 5px;
            color: black;
            transition: all 0.5s;
          }
          .unactive {
            color: #c7c2c2;
          }
        }
      }
      footer {
        display: flex;
        justify-content: flex-end;
        margin-top: 20px;
        .button-group {
          .cancel {
            border: 1px solid rgba(247, 10, 10, 0.842);
            color: rgba(247, 10, 10, 0.842);
            background: #ffffff;
            padding: 10px 20px;
            border-radius: 5px;
            margin-right: 20px;
          }
          .save {
            border: none;
            color: #ffffff;
            background: #0066ff;
            padding: 10px 20px;
            border-radius: 5px;
          }
        }
      }
    }
    .addstretch {
      width: 800px;
    }
  }
}
@media only screen and (max-width: 600px) {
  .gaskir-page {
    .main-menu {
      align-items: center;
      padding: 15px;
      flex-direction: column;
      .list-gas {
        width: 300px;
        margin-bottom: 20px;
      }
      .add-gas {
        width: 330px;
        margin-left: 0;
        .upload {
          .ktp {
            width: 350px;
          }
        }
        .form {
          .form-group {
            input {
              width: 260px;
            }
          }
        }
      }
    }
  }
}
</style>
