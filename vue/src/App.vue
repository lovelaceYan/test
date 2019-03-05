<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button @click="camera()">TAKE PICTURE</button>
    <img id="myImage"></img>

    <b-map-component></b-map-component>
    <router-view/>
  </div>
</template>

<script>
import {cameraTakePicture} from '../static/cordovaplugin.js';
import BMapComponent from './components/BMapComponent.vue';
export default {
  name: 'App',
  data() {
      return {}
  },
  methods:{
    camera:function(){
      cameraTakePicture();
    }
  },
  mounted() {},
  created() {},
  components: {
      BMapComponent
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#myImage {
  width:300px;
  height:200px;
}
</style>
