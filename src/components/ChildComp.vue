<template>
<h2>Child component</h2>
<h3>{{ radhe }}</h3>
<h2 v-for="item in users" :key="item.email">{{ item.name }}</h2>
<button v-on:click="parentFunction()">Click to call parent function</button>

<h2 :class="applyStyle">class Binding</h2>
<button v-on:click="colorful=!colorful">change style</button>
</template>
<script>
export default{
    name:'ChildComp',
    props:{
        radhe:String,
        users:Object,
        parentFunction:Function
    },
    data(){
        return{
            colorful:false
        }
    },
    computed:{
        applyStyle(){
            return{
                green:this.colorful,
                err:true


            }
        }

    }
}
</script>

<style>
.green{
    background-color: green;
    width: auto;
    justify-content: center;

}
.err{
    color:red;
}
</style>
