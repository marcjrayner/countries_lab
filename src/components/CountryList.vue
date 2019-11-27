<template lang="html">
<div>
  <select>
    <option country-list-item v-for ="(country,index) in countries" :country="country" :key="index">{{country.name}}</country-list-item></option>
  </select>

</div>
</template>

<script>
import CountryListItem from './CountryListItem.vue'

export default {
  name: "country-list",
  props: ["countries"],
  components:{
    "country-list-item":CountryListItem
  }

}
</script>

<style lang="css" scoped>
</style>
