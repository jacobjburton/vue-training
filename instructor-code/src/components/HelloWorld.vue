<template>
  <div class="hello">
    <div> This is where we'll start building our project.</div>
    <puppy name="snowflake"></puppy>
    <puppy :name="puppy2"></puppy>
  </div>
</template>

<script>
import puppy from './Puppy';

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      puppy2:'theodore'
    }
  },
  components:{
    puppy:puppy
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
div:hover{
  transition:1s;
  /* transform:rotate(360deg); */
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
