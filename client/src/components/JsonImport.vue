<template>
  <div>
    <!-- <p v-for="dbtr in dbtrs" v-bind:dbtrs="dbtrs" :key="dbtr"> -->
    <p v-bind="dbtrs">{{ dbtrs[0].fileNumber }}</p>
    <p v-bind="dbtrs">{{ dbtrs[1].firstName }}</p>
  </div>
</template>

<script>
import data from "@/assets/dbtr.json";
export default {
  name: "JsonImport",
  computed: {
    dbtrs() {
      return data.dbtrs.map(item => {
        return item;
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
