<template>
<hr/>
<h1>event:</h1>
<button v-on:click="test('dinesh')">Click here</button>
<button v-on:click="test('ganesh')">Click here</button>
<button v-on:dblclick="test('ganesh')">dbl Click here</button>
<hr/>
<h3 v-on:mousemove="moursemoveHandler()">Hover The MOUSE On It</h3>
<div>count: {{count}}</div>
<button v-on:click="Increment">Increment</button>
<button v-on:click="Decrement">Decrement</button>
    <!-- {{arr}}
    {{  
        arr.map((data)=>{
        return <div>{{data}}</div>
        })
    }} -->
<hr/>
<hr/>
</template>

<script>
export default {
    name: 'EventComponent',
    data() {
       return {
        count:0,
        arr:['a','b','c']
       }
    },
    methods: {
        test(name) {
        alert("button is click by"+name)
        },
        moursemoveHandler(){
        console.warn("mouse is move");
        },
         Increment(){
         this.count = this.count + 1
        },
        Decrement(){
            if(this.count >1)
         this.count = this.count - 1;

        },
      }
    }
  
</script>

<style scoped>
h3 {
    color: red;
    background-color:cyan;
    display:inline
}
</style>
