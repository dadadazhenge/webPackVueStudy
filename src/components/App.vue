<template>
    <div>
        <item-list :dataArry="dataArry1" :activeId="activeId1" @active="activeId1=$event"></item-list>
        <!-- <router-link to='/login'>登录</router-link>
        <router-link to='/registry'>注册</router-link>
        <router-view></router-view> -->
    </div>
</template>

<script>
    import itemList from './subComponents/itemList.vue';
    import data from '../js/data.js'

    export default{
        data(){
            return {
                dataArry1:{},
                activeId1:''
            }
        },
        components: {
            itemList
        },
        created(){
            this.dataArry1=data.getData();
            console.log(this.dataArry1)
        },

        methods:{
           
        }
    }
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
    };
</style>