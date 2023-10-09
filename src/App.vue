<template>
  <Greet name="Bruce" heroname="Batman" />
  <Greet name="Yash" heroname="avenger" />
  <Greet name="Gupta" heroname="something" />
  <Greet :name="name" :heroname="channel" />
</template>
<script>
import Greet from './components/icons/Greet.vue'
export default {
  name: 'App',
  components: {
    Greet
  },
  data() {
    return {
      name: 'Vishwas',
      channel: 'codevolution'
    }
  }
}
</script>
