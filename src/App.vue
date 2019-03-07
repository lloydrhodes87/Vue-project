<template>
  <div id="app">
    <h1>Practice Helper</h1>
    <div class="practiceGrid">
      <app-key-center></app-key-center>
      <app-tonality></app-tonality>
      <app-subject></app-subject>
      <app-fretboard-area></app-fretboard-area>
    </div>
  </div>
</template>

<script>
import { eventBus } from "../src/main.js";
import KeyCenter from "../components/KeyCenter.vue";
import Tonality from "../components/Tonailty.vue";
import Subject from "../components/Subject.vue";
import FretboardArea from "../components/FretboardArea.vue";
export default {
  components: {
    appKeyCenter: KeyCenter,
    appTonality: Tonality,
    appSubject: Subject,
    appFretboardArea: FretboardArea
  },
  methods: {
    generate() {
      console.log("hello");
      eventBus.$on("passFunc", generateArea => {
        generateArea();
      });
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

.practiceGrid {
  display: flex;
  margin: 3rem 0;
  justify-content: space-evenly;
}

@media (max-width: 50rem) {
  .practiceGrid {
    flex-direction: column;
  }
}
</style>
