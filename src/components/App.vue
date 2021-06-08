<template>
    <div>
        <ul style="list-style: none">
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='xianhuoping'" @active="curActive='xianhuoping'">
                    <span>
                        <img src="http://121.36.89.165:8080/shopping/resources/style/common/images/icon/default_icon.png" alt="">
                    </span>
                    <span>鲜活品</span>
                </item>
            </li>
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='lengdongping'" @active="curActive='lengdongping'">
                    <span>
                        <img src="http://121.36.89.165:8080/shopping/resources/style/common/images/icon/icon_2.png" alt="">
                    </span>
                    <span>冷冻品</span>
                </item>
            </li>
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='ganzhiping'" @active="curActive='ganzhiping'">
                    <span>
                        <img src="http://121.36.89.165:8080/shopping/resources/style/common/images/icon/icon_3.png" alt="">
                    </span>
                    <span>干制品</span>
                </item>
            </li>
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='yanzhiping'" @active="curActive='yanzhiping'">
                    <span>
                        <img src="http://121.36.89.165:8080/shopping/resources/style/common/images/icon/icon_5.png" alt="">
                    </span>
                    <span>腌制品</span>
                </item>
            </li>
            <li style="width: 180px; height: 35px">
                <item :isActive="curActive==='yumijiyunizhiping'" @active="curActive='yumijiyunizhiping'">
                    <span>
                        <img src="http://121.36.89.165:8080/shopping/resources/style/common/images/icon/icon_7.png" alt="">
                    </span>
                    <span>鱼糜及鱼糜制品</span>
                </item>
            </li>
        </ul>

        <!-- <router-link to='/login'>登录</router-link>
        <router-link to='/registry'>注册</router-link>
        <router-view></router-view> -->
    </div>
</template>

<script>
    import item from './subComponents/item.vue';

    export default{
        data(){
            return {
                curActive: 'xianhuoping'
            }
        },
        components: {
            item
        },
    }
</script>

<style scoped>

    .box{
        width: 180px;
        height: 35px;
    }

    *{
        margin: 0;
        padding: 0;
    };

    a{
        text-decoration: none;
    };
</style>