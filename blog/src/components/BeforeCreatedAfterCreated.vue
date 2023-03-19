<template>
<h1>Before Created And After Created</h1>
<div>{{count}}</div>
<div ref="number">{{number}}</div>
<button v-on:click="count=count+1;number=number+1">increment</button>
<br />
{{mymethod()}}
</template>

<script>
export default {
    name: 'BeforeCreatedAfterCreated',
    data() {
        return {
            count: 0,
            number: 11
        }
    },
    methods: {
        mymethod() {
            // alert("after in mymethod");
            // console.log("methods")
        }

    },
    beforeCreate() {
        // alert("before create");
    },
    created() {
        // alert("after create");
    },
    beforeMount() {
        // alert("before mount");
    },
    mounted() {
        // alert("mount");
    },
    beforeUpdate() {
        // alert("beforeUpdate")
        console.log("b4 update", this.number, this.$refs['number'].textContent);
    },
    updated() {
        // alert("updated")
        console.log("after update", this.number, this.$refs['number'].textContent)
    },
    beforeUnmount(){
        console.log("before unmount")
    },
    unmounted(){
        console.log("unmounted")
    }
}
</script>

<style>
h1 {
    color: orange
}
</style>
