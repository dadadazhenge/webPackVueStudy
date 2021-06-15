<template>
    <div>
        <div class="bodyBox" :style="{width: `${180*column}px`,height:`${height}px`}">
             <item-list :dataArry="dataArry1" :activeId="activeId1" @active="activeId1=$event" :column="column"></item-list>
        </div>
        <div class="fold" :style="{width: `${180*column}px`}" @click="ifFlod=!ifFlod">
            <span>{{ ifFlod?"折叠":"展开" }}</span>
        </div>
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
                activeId1:'',
                column: 2,
                ifFlod: true
            }
        },
        components: {
            itemList,
        },
        created(){
            this.dataArry1=data.getData();
        },

        methods:{
           
        },

        computed: {
            height(){
                var row=2;
                if(this.ifFlod){
                    var row=Math.ceil(this.dataArry1.length/this.column);
                }
                return row*35
            }
        }
    }
</script>

<style scoped>
    .bodyBox{
        overflow: hidden;
        transition: 0.3s;
    }

    .fold{
        height: 35px;
        font-size: 14px;
        color: white;
        background-color: purple;
        line-height: 35px;
        text-align: center;
        user-select: none;
        cursor: pointer;
    }
</style>