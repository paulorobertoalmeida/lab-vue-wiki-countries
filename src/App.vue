<template>
  <div>
    <Navbar title="title" />
    <CountriesList />
  
  <CountryDetails />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import CountriesList from "./components/CountriesList.vue";
import CountryDetails from "./components/CountryDetails.vue";


export default {
  name: 'App',

  components: {
    Navbar,
    CountriesList,
    CountryDetails
},
  data(){
    return {
      title: 'Wiki Country'
    }
  }
};
</script>

<style>
</style>
