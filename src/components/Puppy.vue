<template>
    <div :style="{border:'1px solid ' + color}">
        This is a Puppy
        <input type="color" v-model="color"/>
        <br>
        {{name}} is their name. {{fullName}} is their owner's name.
        <input v-model="owner.first"/>
    </div>
</template>


<script>
    export default {
        name: 'puppy',
        data: function (){
            return {
                test:'Testing',
                color: '#15FFFF',
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
    }
}
</script>


<style>

</style>
