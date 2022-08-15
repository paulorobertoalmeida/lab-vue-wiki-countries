
<script>
export default {
  name: "Navbar",
  props: {},
  data() {
    return {
        title: 'Wiki Countries'
    }
  },
  computed: {},
  methods: {

  }
}
</script>

<template>
  <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-primary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">{{ title }}</a>
      <div className="row">
      <!-- <CountriesList :countries="countries" /> -->
      <!-- <router-view> -->
    </div>
    </div>
  </nav>
</template>

<style >
</style>
