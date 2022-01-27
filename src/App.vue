<template>
  <WordBox v-for='index in guessMatrix.length' :guess='guessMatrix[index]' :key='index'/>
  <KeyRow @keyPress='handleKeypress' :keys='topRow'/>
  <KeyRow @keyPress='handleKeypress' :keys='middleRow'/>
  <KeyRow @keyPress='handleKeypress' :keys='bottomRow'/>
</template>

<script>
import WordBox from './components/WordBox.vue'
import KeyRow from './components/KeyRow.vue'

export default {
  name: 'App',
  components: {
    WordBox,
    KeyRow,
  },
  data(){
    return {
      totalGuesses: 6,
      remainingGuesses: 5,
      guessIndex: 0,
      topRow: [...'qwertyuiop'],
      middleRow: [...'asdfghjkl'],
      bottomRow: ['enter',...'zxcvbnm','delete'],
      guessMatrix: [['','','','',''],['','','','',''],['','','','',''],['','','','',''],['','','','',''],['','','','','']]
    }
  },
  methods: {
    handleKeypress(letter){
      let leng = this.guessMatrix.length
      let guessRow = leng - (this.remainingGuesses) 
      console.log(guessRow)
      this.guessMatrix[guessRow][this.guessIndex] = letter
      this.guessIndex++
      if(this.guessIndex > 4){
        this.remainingGuesses -= 1
        this.guessIndex = 0
      }
      console.log(this.guessMatrix)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Ubuntu Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
