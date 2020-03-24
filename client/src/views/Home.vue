<template>
  <div id="home">
    <div class="home">
      <img alt="Vue logo" src="../assets/mevn.jpg" width="350" />
    </div>
    <DebtorInfo />
  </div>
</template>

<script>
import DebtorInfo from "@/components/DebtorInfo.vue";

export default {
  components: {
    DebtorInfo
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
