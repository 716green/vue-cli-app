<template>
  <div class="debtorList">
    <h2>Debtors</h2>
    <div class="debtorCards" v-for="dbtr in dbtrs">
      <!-- <DebtorCard v-for="dbtr in dbtrs" /> -->
      <DebtorCard> </DebtorCard>

      <!-- </DebtorCard> -->
    </div>
  </div>
</template>

<script>
import DebtorCard from "@/components/DebtorCard.vue";
import data from "@/assets/dbtr.json";
export default {
  name: "DebtorList",
  components: {
    DebtorCard
  },

  computed: {
    dbtrs() {
      return data.dbtrs.map(item => {
        return item;
      });
    }
  }
};
</script>

<style scoped>
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
.debtorList {
  border-style: solid;
  border-width: 1px;
  padding: 10px;
  background-color: #42b983;
  color: whitesmoke;
  border-radius: 1em;
}
.debtorCards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  background-color: darkslateblue;
  padding: 5px;
  border-radius: 1em;
}
</style>
