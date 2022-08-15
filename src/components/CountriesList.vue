<template>
  <div v-for="(country, index) in countries" :key="index">
{{ country.name.common }}

  </div>
</template>

<script>
export default {
  name: "CountriesList",

  components: {},
  data() {
    return {
      //defining an array to fetch api data
      countries: null,
    };
  },
  methods: {
    async fetchCountries() {
      const response = await fetch(
        "https://ih-countries-api.herokuapp.com/countries"
      )
      const finalResponse = await response.json();
      console.log(finalResponse)
      this.countries = finalResponse
    },
  },
  // Using the created hook to make our first call to the db and we add the keyword async before call the hook to secure issues with api calls
  async created() {
    this.fetchCountries();
  },
};
</script>

<style>
</style>