<template>
  <div class="hello">
    <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div>
    <div v-html="channel"></div>
    <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">Click</button>
    <h2 class="underline">underline-text</h2>
    <h2 class="status">status</h2>
    <h2 :class="ispromoted && 'promoted'">movie</h2>
    <h2 :class="isSoldout ? 'soldout' : 'new'">movie</h2>
    <h2 :class="['new', 'promoted']">movie</h2>
    <h2
      :class="{
        promoted: ispromoted,
        new: !isSoldout,
        soldout: isSoldout
      }"
    >
      Object-conditional Movie
    </h2>
    <h2 :style="headerStyleObject">Styling</h2>
    <div :style="[baseStyle, successStyleObject]">Success Style</div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: 'hello',
      name: 'yash',
      channel: '<br>codevolution</br>',
      headingId: 'heading',
      isDisabled: false,
      status: 'danger',
      ispromoted: true,
      isSoldout: true,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyle: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        padding: '20px'
      }
    }
  }
}
</script>
<style scoped>
#app {
  text-align: center;
}
.hello {
  display: flex;
  flex-direction: column;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.soldout {
  color: red;
}
</style>
