<template>
<hr />
<h2>Message from Child !!!</h2>
<h2>user name is : {{name}}</h2>
<h3>user email : {{user.email}} <br />
    user name: {{user.name}}</h3>
<button v-on:click="getData(messageFromChild)">child component</button>
<hr />
</template>

<script>
export default {
    name: 'ChildComponent',
    props: {
        name: String,
        user: Object,
        getData:Function
    },
    data(){
        return {
         messageFromChild:"Message from Child to Parent Component"
        }
    }
}
</script>

<style scoped>
h2 {
    color: red
}
</style>
