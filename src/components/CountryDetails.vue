<template lang="html">
    <div v-if='country'>
        <h3>{{country.name}}</h3>
        <p>Capital City: {{country.capital}} </p>
        <p>Population: {{country.population}}</p>

    </div>
</template>

<script>
import { eventBus } from '../main.js'

export default {
    name: 'country-details',
    props: ['country']

}
</script>

<style>
   
</style>