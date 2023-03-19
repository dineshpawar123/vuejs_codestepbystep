<template>
<hr/>
<h2>Pass Data to Child Component</h2>
<Child name="dinesh" :user="user" :getData="getData"/>
<hr/>
</template>

<script>
import Child from './Child.vue'

export default {
    name: 'ParentToChildDataPass',
    components: {
        Child
    },
    data()
    {
        return{
            user:{name:'peter',email:'peter@test.com'}
        }
    },
    methods:{
        getData(messageFromChild){
            console.warn("parent function called",messageFromChild);
        }
    }
}
</script>

<style>
</style>
