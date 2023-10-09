<template>
  <!-- v-if will run earlier than v-for so dont combine v-if with v-for/ -->
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
  </template>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      names: ['Bruce', 'Clark', 'Diana']
    }
  }
}
</script>
