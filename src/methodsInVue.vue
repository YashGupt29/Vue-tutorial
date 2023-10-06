<template>
  <h2>{{ add(2, 3, 4) }}</h2>
  <h2>{{ multiply(10) }}</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      basemultiplier: 5
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.basemultiplier
    }
  }
}
</script>
