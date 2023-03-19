<template>
<hr/>
<h1>Ref In Vue Js</h1>
<input  type="text" ref="input"/>
<button v-on:click="getData">Click me</button>
<hr/>
</template>

<script>
export default {
    name:'RefInVue1',
    methods:{
        getData()
        {
            this.$refs.input.focus();
            // let input= this.$refs.input.value
            console.log("_________warn",this.$refs.input.value)
            this.$refs.input.style.color ="red";
            this.$refs.input.value =100;
            setTimeout(() => {
                   this.$refs.input.value =300;
            }, 3000);
        }
    }
}
</script>

<style>
h1{
    color:orange
}
</style>