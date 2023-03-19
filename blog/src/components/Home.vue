<template>
<hr/>
{{name='somesh'}}
    <h1>
        Home Component {{studentName}} length: {{studentName.length}}
    </h1>
    <HomeChild msg="HomeChild"></HomeChild>
    <h3>email : {{email}}</h3>
    <h4>{{myFun()}}</h4>
        <h2>{{getName('dinesh from method')}}</h2>
    <h4>{{name}}</h4>
<hr/>
</template>

<script>
import HomeChild from './HomeChild';

export default{
    name:'HomeComponent',
    components:{
    HomeChild
    },
    props:{
        studentName:Array
    },
    data(){
        return{
            email:'dinesh@gmail.com',
            name:'dinesh',
            myFun:()=>{
                return 'This is message from myFunction'
            }
        }
    },
    methods:{
        getName(name)
        {
            return name;
        }
    }

}
</script>

<style scoped>
h3{
    color:green
}

h4{
    color:cyan
}
h3{
    color:green
}

h2{
    color:orange
}
</style>