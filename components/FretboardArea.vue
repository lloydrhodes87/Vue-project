<template>
  <div>
    <h2>Fretboard Area</h2>
    <button @click="generateArea">Change</button>
    <p>{{ area }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      areas: ["Frets: 1-5", "Frets: 5-9", "Frets: 9-14", "Frets: 14+"],
      area: ""
    };
  },
  methods: {
    generateArea() {
      const randomIndex = Math.floor(Math.random() * this.areas.length);
      this.area = this.areas[randomIndex];
    }
  },
  created() {
    this.generateArea();
  }
};
</script>

<style>
</style>