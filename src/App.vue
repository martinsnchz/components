<template>
    <div>
      <h1 class="titre">Biographies d'aviateurs</h1>
      <p class="p1">Choisisez si dessous un aviateur : </p>
      <div class="align">
        <button class="but" v-on:click="component = 'page-wright'">Freres.         .     Wright</button>
        <button class="but" v-on:click="component = 'page-amelia'">Amelia Earhart       .</button>
        <button class="but" v-on:click="component = 'page-gagarine'">Youri Gagarine</button>
        <button class="but" v-on:click="component = 'page-rich'">Manfred von Richthofen</button>
        <button class="but" v-on:click="component = 'page-gor'">Hermann Göring</button>
        <button class="but" v-on:click="component = 'page-lind'">Charles Lindbergh</button>
        </div>
      <br>
      <br>
      <br>
      <component v-bind:is="component"></component>
    </div>
</template>

<script>
// Imports
import wright from './components/wright.vue';
import amelia from './components/amelia.vue'
import gagarine from './components/gagarine.vue'
import richthofen from './components/richthofen.vue'
import goring from './components/goring.vue'
import lindbergh from './components/lindbergh.vue'



export default {
    components: {
        'page-wright': wright,
        'page-amelia': amelia,
        'page-gagarine': gagarine,
        'page-rich': richthofen,
        'page-gor': goring,
        'page-lind': lindbergh
    },
    data () {
        return {
          component: 'page-wright',
        }
    },
}
</script>


<style>
.titre {
    text-align: center;
    font-size: 50pt;
    text-decoration: underline;
}
.titre2 {
    text-align: center;
    font-size: 40pt
}

.align {
  text-align: center;
  font-size: 12pt;
  position:absolute;
  left:33%;
  width:640px;
	height:30px;
}
.img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 40%;
}

.body {
    display: block;
    margin-left: 30px;
    margin-right: 30px;
    font-size: 18pt
}

.but {
  width:100px;
  height:70px;
}


.p1 {
  font-size: 25pt
}
</style>
