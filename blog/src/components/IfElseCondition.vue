<template>
<hr/>
<h1 v-if="show">
    <div>If  Condition</div>
</h1>
<h1 v-else>If Else Condition</h1>
<button v-on:click="toggleIfElse()">{{show}}</button>
<button v-on:click="show=!show">{{show}}</button>
<hr/>
</template>

<script>
export default {
    name: "IfElseCondition",
    data() {
        return {
            show: false
        }
    },
    methods: {
        toggleIfElse() {
           return  this.show = !this.show
        }
    }
}
</script>

<style scoped>
h1 {
    color: 'green'
}
</style>
