<template>
  <div class="debtorCard">
    <!-- <JsonImport v-bind:dbtrs="dbtrs"> -->
    <a class="cardLink" href="#">
      <JsonImport>
        <p v-bind="dbtrs" v-for="dbtr in dbtrs" :key="dbtr.name">
          {{ dbtrs }}
        </p>
      </JsonImport>
    </a>
  </div>
</template>

<script>
import JsonImport from "@/components/JsonImport.vue";
export default {
  name: "DebtorInfo",
  props: {
    dbtrs: Object //Not In Use
  },
  components: {
    JsonImport
  },
  data() {
    return {
      debtors: {
        fileNumber: "123456",
        firstName: "John",
        middleName: "A",
        lastName: "Doe",
        address: "123 Main St",
        address2: "Apt A",
        county: "Bronx",
        city: "Anywhere",
        state: "NY",
        zip: "12345"
      }
    };
  },
  computed: {
    fullName: function() {
      return this.firstName + " " + this.lastName;
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
