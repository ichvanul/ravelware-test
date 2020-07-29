<template>
  <div>
    <section class="sub-menu-a" @click="report">
      <div class="list-menu-a change-a">
        <div class="for-icon"><i class="fas fa-file-invoice"></i></div>
        Pelaporan
      </div>
      <div class="rot ate">
        <i class="fas fa-caret-down"></i>
      </div>
    </section>
    <ul class="list-a hide">
      <li v-bind:class="{ report: isReport == 'type' }" @click="type">
        <p>Kendaraan Per Tipe</p>
      </li>
      <li v-bind:class="{ report: isReport == 'color' }" @click="color">
        <p>Kendaraan Sesuai Warna</p>
      </li>
      <li v-bind:class="{ report: isReport == 'trafic' }" @click="trafic">
        <p>Laporan Trafik</p>
      </li>
      <li v-bind:class="{ report: isReport == 'member' }" @click="member">
        <p>Laporan Member</p>
      </li>
      <li v-bind:class="{ report: isReport == 'custgas' }" @click="custgas">
        <p>Laporan Petugas Parkir</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Report",
  data() {
    return {
      isReport: ""
    };
  },
  methods: {
    report() {
      document.querySelector(".list-a").classList.toggle("hide");
      document.querySelector(".rot").classList.toggle("ate");
    },
    trafic() {
      this.isReport = "trafic";
    },
    income() {
      this.isReport = "income";
    },
    type() {
      this.isReport = "type";
    },
    color() {
      this.isReport = "color";
    },
    member() {
      this.isReport = "member";
    },
    custgas() {
      this.isReport = "custgas";
    }
  }
};
</script>

<style lang="scss" scoped>
.sub-menu-a {
  display: flex;
  justify-content: space-between;
  background: #f2f3f5;
  padding: 10px 15px;
  cursor: pointer;
  .list-menu-a {
    color: #0066ff;
    display: flex;
    .for-icon {
      width: 25px;
    }
  }
  .rot {
    transform: rotate(180deg);
    transition: 0.5s;
  }
  .ate {
    transform: none;
  }
  .change-a {
    color: #000000;
  }
}
.list-a {
  position: relative;
  list-style: none;
  transition: 0.9s;
  li {
    background: #ffffff;
    padding: 5px;
    color: #bababa;
    font-size: 15px;
    cursor: pointer;
    p {
      padding-left: 35px;
    }
  }
  li:hover {
    background: #0066ff;
    color: white;
  }
}
.hide {
  opacity: 0;
  overflow: hidden;
  height: 0;
  transition: 0.5s;
}
.report {
  background: #0066ff !important;
  color: white !important;
}
</style>
