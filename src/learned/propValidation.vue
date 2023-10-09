<template>
  <!-- <Greet name="Bruce" heroname="Batman" />
  <Greet name="Yash" heroname="avenger" />
  <Greet name="Gupta" heroname="something" />
  <Greet :name="name" :heroname="channel" /> -->
  <!-- always add :(v-bind ) to non string props -->
  <Articles title="Artcile Title" :Likes="10" :isPublished="true" />
</template>
<script>
import Articles from '../components/Articles.vue'
export default {
  name: 'App',
  components: {
    Articles
  },
  data() {
    return {
      name: 'Vishwas',
      channel: 'codevolution'
    }
  }
}
</script>
