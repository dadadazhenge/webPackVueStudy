<template>
    <div>
        <ul style="list-style: none">
            <li style="width: 180px; height: 35px" v-for="item in dataArry" :key="item.id">
                <item :isActive="activeId===item.id" @active="$emit('active',item.id)">
                    <span>
                        <img :src="item.src" alt="">
                    </span>
                    <span>{{ item.name }}</span>
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
        },
    methods: {
        
    }
}
</script>

<style>
    *{
        margin: 0;
        padding: 0;
    };
</style>