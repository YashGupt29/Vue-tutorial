<template>
  <h1 v-if="num === 0">The number is 0</h1>
  <h2 v-else-if="num < 0">negative</h2>
  <h2 v-else-if="num > 0">positive</h2>
  <h2 v-else>not a number</h2>
  <template v-if="display">
    <h2>Yash</h2>
    <h2>Gsoc</h2>
    <h2>2024</h2>
  </template>
  <h2 v-show="show">show Element</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      num: 0,
      display: true,
      show: false
    }
  }
}
</script>
