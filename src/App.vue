<template>
  <div id="app">
    <div class="container-fluid">
      <div class="wrapper">
        <canvas class="chart"></canvas>
      </div>
      <h3>{{ isDetails }}</h3>
    </div>
  </div>
</template>

<script>
import {getOSDetails} from './window.js';

export default {
  name: 'app',
  data: function() {
      return {
        isDetails: getOSDetails()
      }
    }
}
</script>

<style>
  #app .container-fluid {
    height: 100%;
    color: white;
    background-color: #111;
  }
  
  #app {
    -webkit-app-region: drag;
  }
  
  .container-fluid {
    padding: 25px;
  }

  .wrapper {
    height: 300px !important;
  }

  h3 {
    text-align: center;
  }
</style>
