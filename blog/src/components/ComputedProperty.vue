<template>
<hr />
<h1>Computed Property</h1>

<!-- <div>Calculation:{{value1+value2+value3*100}}</div>
<div>Calculation:{{value1+value2+value3*100}}</div>
<div>Calculation:{{value1+value2+value3*100}}</div> -->
{{calculation}}
<hr />
</template>

<script>
export default {
    name: "ComputedProperty",
    data() {
        return {
            value1: 10,
            value2: 20,
            value3: 30
        }
    },
    methods: {
        // calculation() {
        //     return this.value1 + this.value2 + this.value3 * 100
        // }
    },
    computed:{
       calculation() {
            return this.value1 + this.value2 + this.value3 * 100
        } 
    }
}
</script>

<style>
h1 {
    color: orange
}
</style>
