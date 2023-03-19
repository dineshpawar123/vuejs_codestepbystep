<template>
<hr/>
<div class="hello">
    <h1>Get CheckBox & Radio Button Value</h1>

    <label for="name">Name : </label>
    <input type="text" v-model="text" placeholder="name" id="name" /><br />

    <label for="name">password : </label>
    <input type="number" v-model="mobNumber" placeholder="enter password" /><br />

    <br />

    <div>Que. What is your favorite programming language ?</div>

    <label for="java">Java</label>
    <input type="checkbox" value="java" v-model="selectedTech" id="java" /><br />

    <label for="php">Php</label>
    <input type="checkbox" value="php" v-model="selectedTech" id="php" /><br />

    <label for="Node">Node</label>
    <input type="checkbox" value="Node" v-model="selectedTech" id="Node" /><br />

    <h4>Selected Technology : {{selectedTech}}</h4>

    <button v-on:click="getData()" type="button">Get Values</button>
    <br/><br/>

    <div>
    <h3>Who I am</h3>
    <label for="student">Student</label>
    <input type="radio" value="student" v-model="whoIAm" id="Node" /><br />

    <label for="student">employee</label>
    <input type="radio" value="employee" v-model="whoIAm" id="employee" /><br />
    </div>
    
<hr/>
    <br /><br />
    {{text}}<br />
    {{mobNumber}}<br />
    {{whoIAm}}<br />
    <br /><br />

</div>
</template>

<script>
export default {
    name: 'GetInputValue',
    data() {
        return {
            text: 'dinesh',
            mobNumber: '9876543210',
            selectedTech:[],
            whoIAm:undefined
        }
    },
    methods: {
        getData() {
            // this.text=this.text 
            console.log("value :", this.text, this.mobNumber)
        }
    }
}
</script>
