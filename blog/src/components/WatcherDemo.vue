<template>
<hr/>
<h1>Watcher Demo</h1>
{{counter}}
<hr/>
</template>

<script>
export default{
    name: "WatcherDemo",
    data(){
       return {counter:0}
    }
}
</script>

<style>
h1{
    color:orange
}
</style>