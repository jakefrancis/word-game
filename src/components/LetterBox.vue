<template>
  <div :class="color">
    {{ letter }}
  </div>
</template>

<script>
export default {
  props: {
    letter: {
        type: String,
        default: ''
    },
    letterState :  {
        type: String,
        default: ''
    }

  },
  data() {
    return {
        
    };
  },
  computed: {
        color: function(){
            if(this.letterState === 'match'){
                return 'green'
            }
            else if(this.letterState === 'contains'){
                return 'yellow'
            }
            else{
                return 'grey'
            }
        }
    }
}
</script>

<style scoped>
div {
  font-size: 2rem;
}

.green {
    color: green;
}

.yellow{
    color: yellow;
}

.grey{
    color: grey;
}
</style>