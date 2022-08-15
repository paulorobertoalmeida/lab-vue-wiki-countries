<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-5 ">
          <div class="list-group d-flex align-items-center ">
            <router-link
              class="list-group-item list-group-item-action justify-content-center "
              v-for="country in countries"
              :to="`/country/${country.alpha3Code}`"
            >
              <img
                :src="`https://flagpedia.net/data/flags/icon/72x54/
${country.alpha2Code.toLowerCase()}.png`"
              />
              <p>{{ country.name.common }}</p>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CountriesList",
  data() {
    return {
      //definimos un valor de datos estilo array para recibir la info del api
      countries: null,
    };
  },
  methods: {
    async fetchCountries() {
      const response = await fetch(
        "https://ih-countries-api.herokuapp.com/countries"
      );
      const finalResponse = await response.json();
      // console.log(finalResponse);//VERIFICAMOS MEDIANTES UNA LLAMADA A CONSOLA QUE RECIBIMOS LOS DATOS
      this.countries = finalResponse;
    },
  },
  //usamos el created hook para hacer nuestra llamada inicial a nuestra base de datos.
  //no usamos async en este caso porque la asincronia la maneja la funcion fetchCountries. El hook created() solo se encarga de llamar la funcion fetchCountries
  created() {
    this.fetchCountries();
  },
};
</script>

<style></style>