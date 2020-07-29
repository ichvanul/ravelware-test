<template>
  <div>
    <section class="sub-menu-c" @click="userAd">
      <div class="list-menu-c" v-bind:class="{ loca: localis == 'loc' }">
        <div class="for-icon"><i class="fas fa-user"></i></div>
        Sistem Admin
      </div>
      <div class="roq qte">
        <i class="fas fa-caret-down"></i>
      </div>
    </section>
    <ul class="list-c hide-c">
      <li v-bind:class="{ admin: isAdmin == 'locir' }" @click="locir">
        <p>Lokir</p>
      </li>
      <li v-bind:class="{ admin: isAdmin == 'user' }" @click="user">
        <p>Pengguna</p>
      </li>
      <li v-bind:class="{ admin: isAdmin == 'hardware' }" @click="hardware">
        <p>Hardware</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "adminSystem",
  data() {
    return {
      isAdmin: ""
    };
  },
  methods: {
    userAd() {
      document.querySelector(".list-c").classList.toggle("hide-c");
      document.querySelector(".roq").classList.toggle("qte");
    },
    locir() {
      this.isAdmin = "locir";
    },
    user() {
      this.isAdmin = "user";
    },
    hardware() {
      this.isAdmin = "hardware";
    }
  }
};
</script>

<style lang="scss" scoped>
.sub-menu-c {
  display: flex;
  justify-content: space-between;
  background: #f2f3f5;
  cursor: pointer;
  padding: 10px 15px;
  .list-menu-c {
    display: flex;
    color: black;
    .for-icon {
      width: 25px;
    }
  }
  .roq {
    transform: rotate(180deg);
    transition: 0.5s;
  }
  .qte {
    transform: none;
  }
}
.list-c {
  list-style: none;
  transition: 1s;
  margin-bottom: 25px;
  li {
    background: #ffffff;
    padding: 5px;
    color: #bababa;
    font-size: 15px;
    transition: 0.5s;
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
.hide-c {
  opacity: 0;
  overflow: hidden;
  height: 0;
}
.admin {
  background: #0066ff !important;
  color: white !important;
}
</style>
