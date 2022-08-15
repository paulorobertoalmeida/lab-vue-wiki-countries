<template>
  <div>
    <Navbar title="title" />
    <CountriesList />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import CountriesList from "./components/CountriesList.vue"
import CountriesList from "./components/CountriesList.vue";

export default {
  name: 'App',

  components: {
    Navbar,
    CountriesList,
    CountriesList
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
