<template>
  <div class="flex">
    <h2>Volume Tracker(0-20)</h2>
    <h3>Current Volume-{{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>
  </div>
</template>
<script>
// use watcher when you have to check any valueif you are ready to perform action
// use of watchers
// when you have to call any api respone to change in data
// when you have to do any transitions
export default {
  name: 'App',
  data() {
    return {
      volume: 0
    }
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('You exceeded 16')
      }
    }
  }
}
</script>
<style scoped>
.flex {
  display: flex;
  flex-direction: column;
}
</style>
