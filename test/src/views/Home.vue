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
        //
        watch:{
            input1(){   
                //데이터를 가지고 function 형식으로 만들 수 있음
                //데이터가 변경되는 걸 캐치해서 알 수 있음
                //(모니터링)
                console.log(this.input1)
            }
        },
        methods:{
            getData(){
                alert(this.input1);
            },
            setData(){
                this.input1="12345";
            }
        },
        //라이프 사이클
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
