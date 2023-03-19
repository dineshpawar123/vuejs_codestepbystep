<template>
<hr/>
<h2>HtmlBinding</h2>
<h2>{{fName}}</h2>
<div v-html="lName">
</div>
<div>{{email}}</div>
<hr/>
</template>

<script>
export default {
    name: 'HtmlBinding',
    // components: {
    //     Child
    // },
    data()
    {
        return{
            fName:'dinesh',
            lName:'<h2>pawar</h2>',
            email:'dinesh@gmail.com'
        }
    },
}
</script>

<style>
</style>
