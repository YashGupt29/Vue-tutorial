<template>
  <h2>{{ name }}</h2>
  <div>
    <button @click="changeName(), increment(1)">Change name</button>
  </div>
  <h2>{{ count }}</h2>
  <button v-on:click="increment(5, $event)">Increase 5</button>
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
    changeName() {
      this.name = 'MF'
    },
    increment(num, event) {
      this.count += num
      console.log(event)
    },
    decrement(num) {
      this.count -= num
    }
  }
}
</script>
