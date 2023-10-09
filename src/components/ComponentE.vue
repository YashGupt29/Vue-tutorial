<template>
  <div>ComponentE</div>
  <ComponentF />
</template>

<script>
import ComponentF from './ComponentF.vue'
export default {
  name: 'ComponentE',
  components: {
    ComponentF
  }
}
</script>

<style lang="scss" scoped></style>
