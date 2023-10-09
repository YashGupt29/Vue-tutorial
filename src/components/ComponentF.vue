<template>
  <div>ComponentF</div>
  <h2>{{ username }}</h2>
</template>

<script>
export default {
  name: 'ComponentF',
  inject: ['username']
}
</script>

<style lang="scss" scoped></style>
