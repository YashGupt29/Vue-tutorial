<template>
  <h2>Hello {{ name }} a.k.a.{{ heroname }}</h2>
</template>
<script>
export default {
  name: 'GreetWord',
  props: ['name', 'heroname']
}
</script>
