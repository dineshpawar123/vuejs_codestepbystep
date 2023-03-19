<template>
<hr/>
<div class="hello">
    <h1>{{ msg }}   </h1>
</div>
<hr/>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg:String
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

