
<script>
export default {
  name: "Navbar",
  props: {},
  data() {
    return {
      title: "Wiki Countries",
    };
  },
  computed: {},
  methods: {},
};
</script>

<template>
  <div>
    <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-primary">
      <div class="container-fluid">
        <router-link class="navbar-brand" to="/list"
          >Wiki Countries
        </router-link>
      </div>
    </nav>
  </div>
</template>


<style >
</style>
