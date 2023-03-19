<template>
<h1>Simple Form</h1>
<form>
<label>Email : </label>
<input type="text" placeholder="Enter Email" v-model="form.email">
<br/><br/>

<label>Password : </label>
<input type="password" placeholder="Enter Password" v-model="form.password">
<br/><br/>

<button type="button" v-on:click="login">Login</button>
</form>
</template>

<script>
export default 
{
    name:"SimpleForm",
    data(){
        return{
            form:{
                email:'',
                password:'',
            
            }
        }
    },
    methods:{
        login(){
          alert("login email",this.form.email,this.form.password);
            console.log("login email",{"email":this.form.email});
        }
    }

}
</script>

<style>
h1{
    color:orange
}
</style>