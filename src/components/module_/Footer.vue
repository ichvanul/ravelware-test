<template>
  <footer>
    <!-- <img src="../../assets/img/logo.png" alt="footer" /> -->
    <h5>Copyright © 2020</h5>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  align-items: center;
  width: 100%;
  height: 70px;
  background: #ffffff;
  box-sizing: border-box;
  img {
    height: 30px;
    margin-left: 25px;
  }
  h5 {
    margin-left: 20px;
    margin-top: -6px;
  }
}
</style>
