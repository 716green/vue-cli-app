<template>
  <div>
    <h2>Debtors</h2>
    <div class="debtorCard">
      <h3>{{ fullName }}</h3>
      <h4>
        {{ address }} {{ address2 }}<br />{{ city }}, {{ state }} {{ zip }}
      </h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "DebtorInfo",
  props: {
    fileNumber: String
  },
  data() {
    return {
      firstName: "John",
      middleName: "A",
      lastName: "Doe",
      address: "123 Main St",
      address2: "Apt A",
      county: "Bronx",
      city: "Anywhere",
      state: "NY",
      zip: "12345"
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
}
</style>
