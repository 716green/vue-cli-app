<template>
  <div class="debtorCard">
    <a class="cardLink" href="#">
      <p>
        <!-- v-bind="dbtr in dbtrs" :key="dbtr"> -->
        {{ dbtrs[0].address }}
      </p>
    </a>
  </div>
</template>

<script>
import data from "@/assets/dbtr.json";
export default {
  name: "DebtorCard",
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

.debtorCard {
  border-style: solid;
  border-width: 1px;
  padding-bottom: 0%;
  border-radius: 1em;
  margin: 5px;
  min-width: 350px;
  flex-grow: 1;
  background-color: slateblue;
}
.cardLink,
a {
  text-decoration: none;
  color: whitesmoke;
}

.debtorCard:hover {
  background: rgba(105, 90, 205, 0.52);
}
</style>
