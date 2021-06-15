<template>
    <div class="item" :class="{active: isActive}" @click="handleClick">
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: [
        "isActive",
    ],
    methods: {
        handleClick(){
            this.$emit("active")
        }
    }
}
</script>

<style scoped>
    a{
        text-decoration: none;
    }


    .item{
        background-color: #e60012;
        width: 100%;
        height: 100%;
        cursor: pointer;
        font-size: 14px;
        line-height: 35px;
        color: white;
        position: relative;
        transition: all 0.2s;
    }

    .active{
        background-color: pink;
    }

    .item:hover{
        background-color: #A8000D;
    }

    .item img{
        position: absolute;
        top: 7px;
        left: 12px;
    }
</style>