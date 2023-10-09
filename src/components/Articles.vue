<template>
  <div>
    <h2>Article Component</h2>
    <h2>{{ title }}</h2>
    <h2>Likes-{{ Likes }}</h2>
    <h2>isPublished-{{ isPublished ? 'yes' : 'no' }}</h2>
  </div>
</template>

<script>
export default {
  name: 'Article',
  props: {
    title: {
      type: String,
      required: true
    },
    Likes: Number,
    isPublished: Boolean
  }
}
</script>

<style></style>
