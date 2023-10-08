<template>
  <h2>Fullname-{{ firstName }} {{ secondName }}</h2>
  <h2>Computed Fullname-{{ fullname }}</h2>
  <h2>
    Total is
    {{ total }}
  </h2>
  <button @click="items.push({ id: 4, title: 'mac', price: 400 })">Add items</button>
  <h2>Total from Method is -{{ getTotal() }}</h2>
  <input type="text" v-model="country" />
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Yash',
      secondName: 'Gupta',
      items: [
        { id: '1', title: 'TV', price: 100 },
        { id: '2', title: 'Mobile', price: 200 },
        { id: '3', title: 'Laptop', price: 300 }
      ],
      country: ''
    }
  },
  // difference between computed and method property is that computed property is cached and not recalculated again but method is recalculated
  // hence improve the performance
  methods: {
    getTotal() {
      console.log('total in method')
      return this.items.reduce((total, curr) => total + curr.price, 0)
    }
  },
  computed: {
    fullname() {
      return `${this.firstName} ${this.secondName}`
    },
    total() {
      console.log('total in computed')
      return this.items.reduce((total, curr) => total + curr.price, 0)
    }
  }
}
</script>
