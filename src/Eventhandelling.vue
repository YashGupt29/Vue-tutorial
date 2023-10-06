<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="name = 'Batman'">Change name</button>
  </div>
  <h2>{{ count }}</h2>
  <button v-on:click="increment(5)">Increase 5</button>
  <button v-on:click="decrement(1)">Decrease 1</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'yash',
      count: 0
    }
  },
  methods: {
    increment(num) {
      this.count += num
    },
    decrement(num) {
      this.count -= num
    }
  }
}
</script>
