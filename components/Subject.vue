<template>
  <div>
    <h2>Subject</h2>
    <button @click="generateSubject">Change</button>
    <p>{{ subject }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subjects: ["Scales", "Arpeggios", "Chords"],
      subject: ""
    };
  },
  methods: {
    generateSubject() {
      const randomIndex = Math.floor(Math.random() * this.subjects.length);
      this.subject = this.subjects[randomIndex];
    }
  },
  created() {
    this.generateSubject();
  }
};
</script>

<style>
</style>