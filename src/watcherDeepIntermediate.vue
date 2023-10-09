<template>
  <div class="flex">
    <h2>Volume Tracker(0-20)</h2>
    <h3>Current Volume-{{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>
    <div>
      <input type="text" v-model="movie" />
      <input type="text" v-model="movieInfo.title" />
      <input type="text" v-model="movieInfo.actors" />
    </div>
    <div>
      <button @click="movieList.push('Wonderwomen')">Add movie</button>
    </div>
  </div>
</template>
<script>
// use watcher when you have to check any valueif you are ready to perform action
// use of watchers
// when you have to call any api respone to change in data
// when you have to do any transitions
//if array will mutate deep is required but when if array is changed to new array deep is not required
export default {
  name: 'App',
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        title: '',
        actors: ''
      },
      movieList: ['Batman', 'Superman']
    }
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('You exceeded 16')
      }
    },
    //intermediate is used to load watcher on page load
    movie: {
      handler(newValue) {
        console.log(`Calling Api with movie name=${newValue}`)
      },
      immediate: true
    },
    //deep is used to load watcher in nester property
    movieInfo: {
      handler(newValue) {
        console.log(`Calling Api with movie title=${newValue.title} and actors=${newValue.actors}`)
      },
      deep: true
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`)
      },
      deep: true
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
