<template>
<BeforeCreatedAfterCreated/>
<ComputedProperty />
<WatcherDemo />
<SimpleFormPartTwo />
<SimpleForm />
<RefInVue1 />
<UserComponent :getUserName="getUserName" />
<!-- <button v-on:click="getUserName()">get data from child to parent</button> -->
{{childUser}}
<ClassBinding />
<ChildToParent />
<HtmlBinding />
<div v-for="item in studentNameArr" :key="item">
    <ReuseComponent :studentNameArr="item" :alertMesssage="alertMesssage" />
</div>

<!-- <ReuseComponent :studentNameArr="studentNameArr"/> -->
<ParentToChildDataPass />
<ForLoop />
<IfElseCondition />
<HelloWorld msg="Welcome to Your Vue.js App" />
<GetInputValue />
{{studentNameArr}}
<Home studentName={{studentNameArr}}></Home>
<EventComponent />
<TwoWayBinding />
<GetInputValue />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Home from './components/Home.vue';
import EventComponent from './components/EventComponent.vue';
import TwoWayBinding from './components/TwoWayBinding.vue';
import GetInputValue from './components/GetInputValue.vue';
import IfElseCondition from './components/IfElseCondition.vue';
import ForLoop from './components/ForLoop.vue';
import ParentToChildDataPass from './components/ParentToChildDataPass.vue';
import ReuseComponent from './components/ReuseComponent.vue';
import HtmlBinding from './components/HtmlBinding.vue';
import ClassBinding from './components/ClassBinding.vue';
import ChildToParent from './components/ChildToParent.vue';
import UserComponent from './components/ChildToParent.vue';
import RefInVue1 from './components/RefInVue.vue';
import SimpleForm from './components/SimpleForm';
import SimpleFormPartTwo from './components/SimpleFormPartTwo';
import ComputedProperty from './components/ComputedProperty';
import WatcherDemo from './components/WatcherDemo';
import BeforeCreatedAfterCreated from './components/BeforeCreatedAfterCreated';

export default {
    name: 'App',
    components: { // registration of component
        HtmlBinding,
        ReuseComponent,
        HelloWorld,
        Home,
        EventComponent,
        TwoWayBinding,
        GetInputValue,
        IfElseCondition,
        ForLoop,
        ParentToChildDataPass,
        ClassBinding,
        ChildToParent,
        UserComponent,
        RefInVue1,
        SimpleForm,
        SimpleFormPartTwo,
        ComputedProperty,
        WatcherDemo,
        BeforeCreatedAfterCreated
    },
    data() {
        return {
            studentNameArr: [{
                    name: 'anil',
                    email: 'anil@gmail.com'
                },
                {
                    name: 'sunil',
                    email: 'sunil@gmail.com'
                },
                {
                    name: 'kapil',
                    email: 'kapil@gmail.com'
                }
            ],
            childUser: ''
        }
    },
    methods: {
        alertMesssage() {
            alert("this is alert message")
        },
        getUserName(name) {
            this.childUser = name
            console.log("==>", name)
            alert(name);
        }
    }
}
</script>
