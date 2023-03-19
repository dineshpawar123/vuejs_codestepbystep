<template>
<h1>Simple Form Part 2</h1>
<div>
    {{form}}
    <br/><br/>
</div>
<form>
    <label>Email : </label>
    <input type="text" placeholder="Enter Email" v-model="form.email">
    <br /><br />

    <label>Password : </label>
    <input type="password" placeholder="Enter Password" v-model="form.password">
    <br /><br />

    Country:
    <select v-model="form.country">
        <!-- <option value="India">India</option> -->
        <option value="India">India</option>
        <option>China</option>
        <option>USA</option>
    </select>

    <br /> <br />
    Technology:
    <br />

    <label>JAVA : </label>
    <input type="checkbox" value="JAVA" v-model="form.technology">
    <br /><br />

    <label>PHP : </label>
    <input type="checkbox" value="PHP" v-model="form.technology">
    <br /><br />

    Gender:
    <label>male  </label>
    <input type="radio" value="male" v-model="form.gender">
    <br /><br />

    <label>female : </label>
    <input type="radio" value="female" v-model="form.gender">
    <br /><br />
    
    <br />

    <button type="button" v-on:click="login">Login</button>
</form>
</template>

<script>
export default {
    name: "SimpleFormPartTwo",
    data() {
        return {
            form: {
                email: '',
                password: '',
                country: '',
                technology: [],
                gender: ''
            }
        }
    },
    methods: {
        login() {
            alert("login email", this.form.email, this.form.password);
            console.log("login email", {
                "email": this.form.email
            });
        }
    }

}
</script>

<style>
h1 {
    color: orange
}
</style>
