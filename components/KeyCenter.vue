<template>
  <div>
    <h2>Key Center</h2>
    <button @click="generateKeyCenter">Change</button>
    <p>{{ chosenKey }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      keyCenters: [
        "A",
        "A#/Bb",
        "B",
        "C",
        "C#/Db",
        "D",
        "D#/Eb",
        "E",
        "F",
        "F#/Gb",
        "G",
        "G#/Ab"
      ],
      chosenKey: ""
    };
  },
  methods: {
    generateKeyCenter() {
      const randomIndex = Math.floor(Math.random() * this.keyCenters.length);
      this.chosenKey = this.keyCenters[randomIndex];
    }
  },
  created() {
    this.generateKeyCenter();
  }
};
</script>

<style>
</style>


