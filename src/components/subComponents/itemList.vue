<template>
    <div>
        <ul style="list-style: none">
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='xianhuoping'" @active="curActive='xianhuoping'">
                    <span>
                        <img :src="dataArry.src" alt="">
                    </span>
                    <span>{{ dataArry.name }}</span>
                </item>
            </li>
    </div>
</template>

<script>
import item from './itemList.vue';

export default {
    data(){
        return {
            curActive: 'xianhuoping'
        }
    },
    components: {
        item
    },
    props: {
        dataArry: {
            type: Object,
            default: function(){
                return {};
            }
        }
    }
}
</script>

<style>
    
</style>