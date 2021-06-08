<template>
    <div>
        <!-- <router-link to='/login'>登录</router-link>
        <router-link to='/registry'>注册</router-link>
        <router-view></router-view> -->
    </div>
</template>

<script>
    import itemList from './subComponents/itemList.vue'
    export default{
        data(){
            return {

            }
        },
        components: {
            itemList
        }
    }
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
    };
</style>