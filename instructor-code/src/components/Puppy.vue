<template>
  <div :style="{border:'1px solid '+color}">
    This is an amazing puppy!!!! 
    <input type="color" v-model="color"/>
    <br>
    {{name}} is their name.  {{fullName}} is their owner's name.
    <input v-model="owner.first"/>
  </div>
</template>

<script>
export default { 
  name:'puppy',
  data:function() {
    return {
      test:'This is a test',
      color:'#15FFFF',
      owner:{
        first:'Bob',
        last:'Not the builder cause copyright and stuff'
      }
    }
  },
  props:{
    name:String
  },
  computed:{
    fullName:function(){
      console.log('what?');
      return this.owner.first + ' ' + this.owner.last;
    }
  },
  mounted: function () {
    console.log("Component did mount");
  }
}
</script>

<style>

</style>
