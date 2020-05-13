<template>
  <div>
    <h1>Countries App</h1>
    <countries-list :countries='countries'></countries-list>
  </div>
</template>

<script>
import CountriesList from './components/CountryList.vue';

export default {
  name: 'app',
  data(){
    return {
      countries: [],
      selectedCountry: null
    };
  },
  mounted(){
    fetch('https://restcountries.eu/rest/v2/all')
    .then(resourses => resourses.json())
    .then(countries => this.countries = countries)
  },
  components: {
    "countries-list": CountriesList
  }

}

</script>

<style>

</style>
