<template>
  <div class="form-page">
    <section class="title">
      <h1>Input Data Mobil Masuk</h1>
    </section>
    <div class="input-car" v-bind:class="{ addexpand: expanded }">
      <section class="form">
        <div class="form-group">
          <label for="number">Nomor Polisi</label>
          <input type="text" id="number" />
        </div>
        <div class="form-group">
          <label for="color">Tanggal Masuk</label>
          <input type="text" id="color" />
        </div>
        <div class="form-group">
          <label for="type">Tipe Mobil</label>
          <input type="text" id="type" />
        </div>
        <div class="form-group">
          <label for="date">Jam Masuk</label>
          <input type="text" id="date" />
        </div>
        <div class="form-group">
          <label for="no">Warna Mobil</label>
          <input type="text" id="no" />
        </div>
      </section>
      <div class="button-group">
        <button class="save">SIMPAN</button>
        <button class="cancel">HAPUS</button>
      </div>
      <h3>Informasi Karcis</h3>
      <section class="ticket">
        <div class="park">
          <h1>Karcis Parkir Mobil</h1>
          <p class="info">No. Polisi: B 1234 KB</p>
          <p class="info">Tempat Parkir: A1</p>
          <P class="info">Tanggal & Jam Masuk: 2020-07-07 07:00</P>
          <p class="note">
            Perhatian: Harap menunjukkan karcis saat meninggalkan area Parkir.
            Jangan meninggalkan barang berharga di dalam kendaraan.
          </p>
        </div>
      </section>
      <div class="button-group">
        <button class="print">CETAK</button>
        <button class="cancel">BATAL</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Form",
  props: ["expanded"]
};
</script>

<style lang="scss" scoped>
.form-page {
  display: none;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .input-car {
    background: white;
    width: 1060px;
    margin-left: 30px;
    margin-bottom: 50px;
    border-radius: 10px;
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
    padding: 20px;
    box-sizing: border-box;
    transition: 0.5s;
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
          width: 470px;
          height: 35px;
          margin: 5px 0;
        }
      }
    }
    h3 {
      margin-top: 10px;
    }
    .ticket {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 380px;
      border: 1px solid #c7c2c2;
      border-radius: 8px;
      padding: 20px;
      box-sizing: border-box;
      margin-top: 10px;
      h1 {
        margin-bottom: 5px;
      }
      .info {
        margin-bottom: 10px;
      }
      .note {
        font-size: 10px;
      }
    }
    .button-group {
      margin-top: 20px;
      .cancel {
        border: 1px solid rgba(247, 10, 10, 0.842);
        color: rgba(247, 10, 10, 0.842);
        background: #ffffff;
        padding: 10px 20px;
        border-radius: 5px;
        margin-left: 20px;
        cursor: pointer;
      }
      .print {
        border: none;
        color: #ffffff;
        background: #0066ff;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
      }
      .save {
        border: none;
        color: #ffffff;
        background: #0066ff;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
      }
    }
  }
  .addexpand {
    width: 1290px;
    .form {
      .form-group {
        input {
          width: 590px;
        }
      }
    }
  }
}
</style>
