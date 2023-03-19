<template>
<hr/>
<h2>Class Binding</h2>
<h2 :class="{green:greenBack,width:true}">{{fName}}</h2>

<button v-on:click="greenBack=!greenBack">toggle back color</button>
<div v-html="lName"></div>
<hr/>
</template>

<script>
export default {
    name: 'ClassBinding',
    data()
    {
        return{
            fName:'dinesh',
            lName:'<h2>pawar</h2>',
            greenBack:false,
        }
    },
}
</script>

<style>
    .green{
        background-color:green;
        padding:10px;
        color:white
    }
    .width{
       width:200px
    }
</style>
