<template>
    <div>
      <button v-on:click="component = 'page-wright'">Freres</button>
      <button v-on:click="component = 'page-amelia'">Amelia</button>
      <component v-bind:is="component"></component>
      <img :src="img">
    </div>
</template>

<script>
// Imports
import wright from './components/wright.vue';
import amelia from './components/amelia.vue'


export default {
    components: {
        'page-wright': wright,
        'page-amelia': amelia
    },
    data () {
        return {
          component: 'page-wright',
          img: require('./assets/image1.jpg'),
        }
    },
}
</script>

<style>
</style>
