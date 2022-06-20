<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>Test chart.js with Vue</h1>
  <div class="float-container">
    <BarChart />
    <MyBar />
    <MyPie />
    <MyLine />
    <MyRadar />
  </div>
</template>

<script>
import BarChart from "./components/BarChart.vue";
import MyBar from "./components/MyBar.vue";
import MyPie from "./components/MyPie.vue";
import MyLine from "./components/MyLine.vue";
import MyRadar from "./components/MyRadar.vue";

export default {
  name: "App",
  components: {
    BarChart,
    MyBar,
    MyPie,
    MyLine,
    MyRadar,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
