<template>
<h2> User Component </h2>
<h3>Passing data from child to parent</h3>
<button v-on:click="getUserName(userName)">get data in child</button>
</template>

<script>
export default{
    name:"UserComponent",
    data(){
        return{
            userName:"Data Send from child to parent"
        }
    },
    props:{
        getUserName:Function
    }
}
</script>

<style>
</style>

