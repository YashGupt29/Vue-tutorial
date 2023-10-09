<template>
  <h2>Component name-{{ name }}</h2>
  <ComponentC />
</template>
<script>
import ComponentC from './components/Componentc.vue'
export default {
  name: 'App',
  components: { ComponentC },
  data() {
    return {
      name: 'Yash'
    }
  },
  provide() {
    return {
      username: this.name
    }
  }
}
</script>
