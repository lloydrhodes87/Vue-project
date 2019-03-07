<template>
  <div>
    <h2>Tonality</h2>
    <button @click="generateTonality">Change</button>
    <p>{{ tonality }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tonalities: ["Major", "Minor"],
      tonality: ""
    };
  },
  methods: {
    generateTonality() {
      const randomIndex = Math.floor(Math.random() * this.tonalities.length);
      this.tonality = this.tonalities[randomIndex];
    }
  },
  created() {
    this.generateTonality();
  }
};
</script>

<style>
</style>


