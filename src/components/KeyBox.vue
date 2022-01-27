<template>
  <div @click="$emit('keyPress',this.letter)">
    {{ letter }}
  </div>
</template>

<script>
export default {
  props: {
    letter: {
      type: String,
      default: ''
    }
  },
  methods: {

  }
}
</script>

<style scoped>
div {
  font-size: 2rem;
  background: lightblue;
  padding: 5px 10px;
  border-radius: 10px;
  height: 2rem;
  cursor: pointer;
}


</style>