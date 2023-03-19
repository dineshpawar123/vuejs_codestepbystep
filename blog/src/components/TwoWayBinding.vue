<template>
<hr/>
<div class="hello">
    <h1>Two Way Binding</h1>
    <input type="text" v-model="text"/>
    <input type="number" v-model="mobNumber"/>
    <select v-model="selectOption">
    <option value="option 1">option 1</option>
    <option value="option 2">option 2</option>
    <option value="option 1">option 1</option>
    <option value="option 2">option 2</option>
    </select>
    <br/><br/>
       
    {{text}}
    {{mobNumber}}
    {{selectOption}}
    <hr/>
</div>
</template>

<script>
    export default {
        name: 'TwoWayBinding',
        data(){
            return{
                text:'dinesh',
                mobNumber:'9876543210',
                selectOption:'option 1'
            }
        },
        methods:{
            // setInputText(){
            //     this.text=this.text + currentValue
            // }
        }
    }
</script>


<style>
</style>
