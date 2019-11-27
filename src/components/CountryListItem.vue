<template lang="html">

<option v-on:click="handleClick" >{{country.name}}</option>

</template>

<script>

import{eventBus} from '../main.js';

export default {
  name:"country-list-item",
  props:["country"],
  methods:{ handleClick(){
    // console.log('country', this.country)}
    eventBus.$emit("country-selected",this.country)
  },

}


}

</script>

<style lang="css" scoped>
</style>
