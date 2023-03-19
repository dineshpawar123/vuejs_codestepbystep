<template>
<hr/>
<h1>I am {{msg}}</h1>
<h3>
<i>firstName:</i> {{getData().firstName}} <br/>
<i>lastName:</i> {{getData().lastName}}
</h3>
<hr/>
</template>

<script>
export default {
    name: 'HomeChild',
    props: {
        msg: String
    },
    methods: {
        getData() {
            return {
                firstName:'dinesh',
                lastName:'pawar',
            }
        }
    }
}
</script>

<style scoped>
h1 {
    color: red
}
</style>
