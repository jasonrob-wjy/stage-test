<template>
  <div id="app">
    <textarea id="input" style="width:100%;height:45%;"></textarea>
    <div style="margin:0px auto;"><input type="button" id="btnFormat" @click="forXml" value="格式化" style="width:50%;height:10%;"/></div>
    <textarea id="output" style="width:100%;height:45%;"></textarea>
    <router-view/>
  </div>
</template>

<script>
import {formatXml} from './formateXml.js'
export default {
  name: 'App',
  data() {
    return {

    }
  },
  methods:{
    forXml() {
      document.getElementById('output').value = formatXml(document.getElementById('input').value);
    },
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
</style>
