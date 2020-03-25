<template>
  <div class="debtorCard">
    <a class="cardLink" href="#">
      <h3>
        {{ debtors.fileNumber }} <br />{{ debtors.firstName }}
        {{ debtors.lastName }}
      </h3>
      <h4>
        {{ debtors.address }} {{ debtors.address2 }}<br />{{ debtors.city }},
        {{ debtors.state }} {{ debtors.zip }}
      </h4>
    </a>
  </div>
</template>

<script>
//import dbtr from "@/dbtr.json";
export default {
  name: "DebtorInfo",
  props: {
    dbtr: Object //Not In Use
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
