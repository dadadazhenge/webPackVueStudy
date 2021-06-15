<template>
    <div>
        <ul style="list-style: none" class="dataUl">
            <li class="dataList" :style="{width: `${100/column}%`}" v-for="item in dataArry" :key="item.id">
                <item :isActive="activeId===item.id" @active="$emit('active',item.id)">
                    <span>
                        <img :src="item.src" alt="">
                    </span>
                    <span class="dataSpan">{{ item.name }}</span>
                </item>
            </li>
        </ul>
    </div>
</template>

<script>
import item from './item.vue';

export default {
    data(){
        return {
            
        }
    },
    components: {
        item
    },
    props: 
        {   
            dataArry: Array,
            activeId: String, 
            column: Number      
        },
    methods: {
        
    }
}
</script>

<style scoped>
    .dataUl{
       overflow: hidden;
    }


    .dataList{
        float: left;
        height: 35px;
    }

    .dataSpan{
        margin-left: 40px;
    }
</style>