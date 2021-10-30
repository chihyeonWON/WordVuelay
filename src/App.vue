<template>
  <div id="root">
    <form>
      <input type="text">
      <button type="submit">입력</button>
    </form>
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

  },
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
