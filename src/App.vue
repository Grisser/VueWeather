<template>
  <div id="app">
    <WeatherWidget
      v-bind:temperature-feel="temperatureFeel"
      v-bind:temperature-real="temperatureReal"
      v-bind:humidity="humidity"
      v-bind:wind="wind"
      />
  </div>
</template>

<script>
import WeatherWidget from "./components/WeatherWidget";

export default {
  name: 'app',
  components: {
    WeatherWidget
  },
  data() {
    return {
      temperatureReal: 1,
      temperatureFeel: '-3.2',
      humidity: 6,
      wind: 20
    }
  }
}
</script>

<style>
  body {
    margin: 0;
    padding: 0;
  }

  #app {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background: rgb(244, 123, 186);
    background: linear-gradient(-25deg, rgba(244, 123, 186, 0.5) 20%, rgba(90, 95, 245, 0.5) 80%);
  }
</style>
