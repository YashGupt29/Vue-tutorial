<template>
  <!-- <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2> -->
  <!-- <h2 v-for="name in fullName" :key="name">{{ name.firstName }} {{ name.secondName }}</h2> -->
  <div class="out">
    <div v-for="actor in actors" :key="actor">
      <h2>{{ actor.name }}</h2>
      <h2 v-for="movie in actor.movies" :key="movie">{{ movie }}</h2>
    </div>
    <h2 v-for="value in myInfo" :key="value">{{ value }}</h2>
    <template v-for="name in names" :key="name">
      {{ name }}
      <hr />
    </template>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      names: ['yash', 'anurag', 'vasu'],
      fullName: [
        { firstName: 'yash', secondName: 'Gupta' },
        { firstName: 'anurag', secondName: 'Bhandari' },
        { firstName: 'vasu', secondName: 'sharma' }
      ],
      actors: [
        { name: 'Christian Bale', movies: ['Batman', 'The Prestige'] },
        { name: 'Di Caprio', movies: ['titanic', 'Inception'] }
      ],
      myInfo: {
        name: 'yash',
        channel: 'Codevolution',
        course: 'Vue 3'
      }
    }
  }
}
</script>
<style scoped>
.out {
  display: flex;
  flex-direction: column;
}
</style>
