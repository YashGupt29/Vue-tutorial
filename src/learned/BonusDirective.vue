<template>
  <h2>{{ name }}</h2>
  <!-- v-once directive is used to not re-render the component as useMemo in react -->
  <button @click="name = 'lund'" v-once>Change Name</button>
  <!-- v-pre directive is used to not to compile the javascript -->
  <h2 v-pre>{{ name }}</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'yash'
    }
  },
  methods: {}
}
</script>
