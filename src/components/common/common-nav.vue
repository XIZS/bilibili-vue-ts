<template>
    <nav class="common-nav">
        <div class="left">
            <ul>
                <li to >
                    <i class="iconfont icon-bilibili-fill" style="margin-right:5px;"></i> 主站
                </li>
                <li to>番剧</li>
                <li to>游戏中心</li>
                <li to>直播</li>
                <li to>会员购</li>
                <li to>漫画</li>
                <li to>赛事</li>
                <li to>
                    <i class="iconfont icon-phone"></i>下载APP
                </li>
            </ul>
        </div>
        <div class="middle">
            <div class="search">
                <!-- TODO 下面input内容为remote调用 -->
                <input type="text" name id placeholder="青你2训练生绝美群像" />
                <div class="btn">
                    <i class="iconfont icon-search"></i>
                </div>
            </div>
        </div>
        <div class="right">
            <ul>
                <li>
                    <div class="search-btn" style="color:black">
                        <i class="iconfont icon-search"></i>
                    </div>
                </li>
                <li style="width:36px;height:36px;">
                    <div class="avatar">
                        <img
                            src="http://i0.hdslb.com/bfs/face/96dedf9951ec18abf83d64a7664f1f4438c8e512.jpg@70w_70h_1c_100q.webp"
                            alt
                        />
                    </div>
                    <nav-bubble></nav-bubble>
                </li>
                <li>大会员</li>
                <li>消息</li>
                <li>动态</li>
                <li>收藏</li>
                <li>历史</li>
                <li>创作中心</li>
                <li>
                    <bili-button
                        @click="contribute"
                        style="width:100px;background:#fb7299;height:100%;display:flex;align-items:center;justify-content:center;border-radius:2px;"
                    >投稿</bili-button>
                </li>
            </ul>
        </div>
    </nav>
</template>


<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import BiliButton from "@/components/common/bili-button.vue";
import NavBubble from "@/components/common/nav-bubble.vue";
@Component({
    components: {
        BiliButton,
        NavBubble
    }
})
export default class ClassName extends Vue {
    private contribute() {
        console.log("aa");
    }
}
</script>


<style lang="scss" scoped>
.common-nav {
    display: flex;
    justify-content: space-between;
    font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", Helvetica,
        Arial, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif;
    font-size: 14px;
    padding: 10px 24px;
    color: white;
    text-shadow: 0 1px 1px rgba(0, 0, 0, 0.3);
    width: 100vw;
    height: 56px;
    box-sizing: border-box;
    position: relative;
    & > * {
        flex: 1;
    }

    .left ul {
        height: 100%;
        display: flex;
        position: relative;
        li {
            white-space: nowrap;
            margin-right: 12px;
            display: flex;
            align-items: center;

            .iconfont {
                font-size: 18px;
            }
        }
    }
    .middle {
        @media screen and (max-width: 1110px) {
            display: none;
        }
        width: 500px;
        flex: initial;
        margin: 0 10px;

        .search {
            display: flex;
            border-radius: 3px;
            height: 100%;
            overflow: hidden;

            input {
                outline: none;
                border: none;
                padding: 0 15px;
                width: 100%;
                background: #eee;
            }
            .btn {
                flex-shrink: 0;
                background: #e7e7e7;
                display: flex;
                align-items: center;
                width: 48px;
                justify-content: center;

                .iconfont {
                    font-size: 18px;
                    color: #505050;
                }
            }
        }
    }

    .right {
        ul {
            display: flex;
            justify-content: flex-end;
        }

        .search-btn {
            display: none;
            .iconfont {
                color: white;
                font-size: 20px;
            }
            @media screen and (max-width: 1110px) {
                display: inline;
            }
        }

        li {
            display: flex;
            align-items: center;
            margin-left: 12px;
            white-space: nowrap;
            .avatar {
                border-radius: 100%;
                height: 100%;
                overflow: hidden;
                img {
                    height: 100%;
                }
            }
        }
    }
}
</style>