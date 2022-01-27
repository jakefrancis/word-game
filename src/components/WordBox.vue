<template>
    <div class='wordbox-container'>
        <LetterBox v-for='letter, index  of guess' :letter='letter' letterState='match' :key='index'/>
    </div>
</template>

<script>
import LetterBox from './LetterBox'

export default {
    components: {
        LetterBox
    },
    props: {
      guess: {
        type: Array,
      }
    },
    mounted(){
      console.log(this.guess)
    }
}
</script>

<style scoped>
.wordbox-container{
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  margin: 0 auto;
  width: 40%;
  min-width: 200px;
  padding: 0.5rem;
}

</style>