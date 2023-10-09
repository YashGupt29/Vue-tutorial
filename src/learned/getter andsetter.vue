<template>
  <h2>Fullname-{{ firstName }} {{ secondName }}</h2>
  <!-- <h2>Computed Fullname-{{ fullname }}</h2> -->
  <button @click="changefullName">ChangeFull Name</button>
  <h2>
    Total is
    {{ total }}
  </h2>
  <button @click="items.push({ id: 4, title: 'mac', price: 400 })">Add items</button>
  <h2>Total from Method is -{{ getTotal() }}</h2>
  <input type="text" v-model="country" />
  <template v-for="item in items" :key="item.id">
    <div v-if="item.price > 100">{{ item.title }}</div>
  </template>
  <h2 v-for="item in expensive" :key="item.id">{{ item.price }} {{ item.title }}</h2>
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
    },
    changefullName() {
      return (this.fullname = 'Angela White')
    }
  },
  computed: {
    fullname: {
      get() {
        return `${this.firstName} ${this.secondName}`
      },
      set(value) {
        const name = value.split(',')
        this.firstName = name[0]
        this.secondName = name[1]
      }
    },
    total() {
      console.log('total in computed')
      return this.items.reduce((total, curr) => total + curr.price, 0)
    },
    expensive() {
      return this.items.filter((item) => item.price > 100)
    }
  }
}
</script>
