<template>
  <div id="root">
    제시어 : {{ word }}
    <form v-on:submit="onSubmitForm">
      <input type="text" v-model="inputValue" ref="answer">
      <button type="submit">입력</button>
    </form>
  </div>
  <div> 
    {{ result }}
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      word:'끝말잇기',
      inputValue:'',
      result:'',
    }
  },
  methods:{
    onSubmitForm(e){
      e.preventDefault();
      if(this.word[this.word.length - 1] === this.inputValue[0]) {
        this.result = '정답';
        this.word = this.inputValue;
        this.inputValue = '';
        this.$refs.answer.focus();
      } else {
        this.result = '땡';
        this.inputValue='';
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

body {
  margin:0;
  padding:0;
}
</style>
