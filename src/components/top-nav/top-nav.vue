<template>
  <div class="top-nav">
    <div class="nav-inner">
      <div><img class="logo" src="../../assets/logo-white.svg" alt="" /></div>
    </div>
  </div>
</template>
<script>
// import { topNav } from "../../components/top-nav/top-nav.vue";
export default {
  name: "TopNav",
  //   components: {
  //     topNav,
  //   },
};
</script>
<style lang="scss" scoped>
.top-nav {
  .nav-inner {
    background-color: #091b1f;
    padding: 20px 70px;
    display: flex;
    // border-bottom: 1px;

    .logo{
            width: 90px;
    }
  }
}
</style>