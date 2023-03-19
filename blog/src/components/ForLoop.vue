<template>
<hr/>
    <div><b>List Of City :</b></div>
    <div>
        <ul v-for="item in listOfCity" :key="item">
          <li>{{item}}</li>
        </ul>
         <ul v-for="item of listOfCity" :key="item">
          <li v-on:click="deleteCity(item)">{{item}}</li>
        </ul>
    </div>
    <div><b>User Name and City :</b></div>
    <div>
        <ul v-for="value in arrayOfObject" :key="value.id">
          <li v-on:click="deleteUser(value.id)">{{value.name}} : {{value.city}}</li>
        </ul>
    </div>
    <hr/>
<!-- {{
    for(let i=0;i<5;i++)
    {
        return <div>listOfCity[i]</div>
    }
}} -->
</template>

<script>
export default {
    name: 'ForLoop',
    data() {
        return{
            listOfCity:['pune','mumbai','nashik','delhi'] ,
            arrayOfObject:[
                {name:'dinesh',city:'pune',id:1},
                {name:'ganesh',city:'pune',id:1},
                {name:'yogesh',city:'pune',id:2}
            ],     
        }
    },
    methods:{
        deleteCity(item){
            console.log("city deleted",item);
          this.listOfCity=  this.listOfCity.filter((data)=>{
                return data != item
            })
        },
        deleteUser(key){
                  console.log("city deleted",key);
        }
    }
}
</script>

<style scoped>
h1 {
    color: orange
}
</style>
