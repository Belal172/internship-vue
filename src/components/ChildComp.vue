<template>
<h2>Child component</h2>
<h3>{{ radhe }}</h3>
<h2 v-for="item in users" :key="item.email">{{ item.name }}</h2>
<button v-on:click="parentFunction()">Click to call parent function</button>
</template>
<script>
export default{
    name:'ChildComp',
    props:{
        radhe:String,
        users:Object,
        parentFunction:Function
    }
}
</script>
