<template>
    <div class="home">
        <!-- 这个页面是网站的首页..内容包括 顶部的导航栏,banner,频道导航栏,推荐(轮播图,推荐商品) -->
        <home-head></home-head>

        <!-- 导航栏,特征:在首页的时候position为absolute,其他状态为relative -->
    </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HomeHead from "@/components/home/home-head.vue";

@Component({
    components:{
        HomeHead
    }
})
export default class Home extends Vue {}
</script>
