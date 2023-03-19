<template>
<hr />
<!-- {{studentNameArr}} -->
<div><b>* Email List of Users : </b></div>
<ul>
    <li>{{studentNameArr.name}}</li>
    <li>{{studentNameArr.email}}</li>
    <button v-on:click="alertMesssage">Click here</button>
</ul>
<hr />
</template>

<script>
export default {
    name: 'ReuseComponent',
    props: {
        studentNameArr: Object,
        alertMesssage:Function
    },
    data() {
    },
    methods: {
        // alertMesssage(){
        //     alert("this is alert message")
        // }
    }
}
</script>

<style scoped>
ul{
    color: blue;
    background-color:cyan
}
</style>
