<template>
  <div>ComponentC</div>
  <ComponentE />
</template>

<script>
import ComponentE from './ComponentE.vue'
export default {
  name: 'ComponentC',
  components: {
    ComponentE
  }
}
</script>

<style lang="scss" scoped></style>
