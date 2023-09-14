<template>
    <div>
        <h1>Welcome to {{title}} in {{title2}}</h1>
        <input type="text" v-model="input1"/>
        <button type="button" @click="getData">Get</button>
        <button type="button" @click="setData">Set</button>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                title:"haha",
                title2:"Seoul",
                input1:"",
            };
        },
        methods:{
            getData(){
                alert(this.input1);
            },
            setData(){
                this.input1="12345";
            }
        },
        beforeCreate(){
            console.log("beforeCreate")
        },
        created(){
            console.log("created")
        },
        beforeMount(){
            console.log("beforeMount")
        },
        mounted(){
            console.log("mount")
        },
        beforeUpdate(){
            console.log("beforeUpdate")
        },
        updated(){
            console.log("updated")
        },
        beforeDestroy(){
            console.log("beforeDestroy")
        },
        destroyed(){
            console.log("destroyed")
        }
    }
</script>
