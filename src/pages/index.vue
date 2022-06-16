<script setup lang="ts">
const menu = reactive([
    {
        id: 0,
        name: '推荐',
        path: '/',
    },
    {
        id: 1,
        name: '排行榜',
        path: '/category',
    },
    {
        id: 2,
        name: '歌单',
        path: '/rank',
    },
    {
        id: 3,
        name: '歌手',
        path: '/search',
    },
])

const url = 'http://localhost:3000/song/url?id=33894312&proxy=http://121.196.226.246:84'
const { isFetching, error, data } = await useFetch(url)
</script>

<template>
    <div>
        <!-- 容器 -->
        <div
            border-solid
            border-red-500
            border-1
            w-screen
            h-screen
            flex
            flex-col
        >
            <!-- 上部分 -->
            <div
                flex-1
                flex
            >
                <!-- 左侧 -->
                <div
                    w-170px
                    border-r
                    border="~ solid [#f5f5f5]"
                    p="l-25px"
                >
                    <!-- logo -->
                    <div
                        h-67px
                        flex
                        flex-col
                        justify-center
                        items-start
                    >
                        <img src="./../assets/img/logo.svg" alt="logo" />
                    </div>
                    <!-- menu -->
                    <div
                        flex
                        justify-start
                        m-t-33px
                    >
                        <ul
                            flex-1
                            flex
                            flex-col
                            items-start
                        >
                            <li
                                v-for="item in menu"
                                :key="item.id"
                                p="10px 0"
                            >
                                {{ item.name }}
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- 右侧 -->
                <div
                    flex-1
                    flex
                    flex-col
                >
                    <!-- 头部 -->
                    <div
                        p-l-22px
                        h-67px
                        flex
                        justify="start"
                        items-center
                    >
                        <div
                            flex
                            justify="start"
                            items-center
                            flex-1
                        >
                            <img src="./../assets/img/serch.svg" alt="搜索" w-18px h-21px m-r-10px />
                            <input type="text" placeholder="搜索歌曲" border-0 />
                        </div>
                        <div
                            w-507px
                            h-67px
                            flex
                        >
                            <ul
                                flex
                                flex-row
                                justify-center
                            >
                                <li
                                    flex
                                    items-center
                                    justify="center"
                                    w-87px
                                    border-r
                                    border-l
                                    border="[#f5f5f5]"
                                >
                                    TV
                                </li>
                                <li
                                    flex
                                    items-center
                                    justify="center"
                                    w-87px
                                    border-r
                                    border="[#f5f5f5]"
                                >
                                    2
                                </li>
                                <li
                                    flex
                                    items-center
                                    justify="center"
                                    w-87px
                                    border-r
                                    border="[#f5f5f5]"
                                >
                                    3
                                </li>
                            </ul>
                            <!-- 头像 -->
                            <div
                                flex
                                flex-row
                                justify-center
                                items-center
                                m-l-23px
                            >
                                <img src="./../assets/img/avatar.svg" alt="头像" color="red" w-50px h-50px />
                                <div>
                                    <span>登录</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- swiper -->
                    <div
                        h-307px
                        flex
                        justify="center"
                    >
                        <img src="https://pic1.zhimg.com/50/v2-e57478a346f75a31bce1511fca743fb9_720w.jpg" h-307px alt="" />
                    </div>
                    <!-- main -->
                    <div
                        flex-1
                    >
                        1
                    </div>
                </div>
            </div>
            <!-- 底部 -->
            <div
                h-62px
                bg-gray-500
            >
                2
            </div>
        </div>
        <!-- <div i-carbon-campsite text-4xl inline-block />
        <p>
            <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">
                Vitesse Lite
            </a>
        </p>
        <p>
            <em text-sm op75>Opinionated Vite Starter Template</em>
        </p>

        <div py-4 />

        <input
            id="input"
            v-model="name"
            placeholder="What's your name?"
            type="text"
            autocomplete="false"
            p="x-4 y-2"
            w="250px"
            text="center"
            bg="transparent"
            border="~ rounded gray-200 dark:gray-700"
            outline="none active:none"
            @keydown.enter="go"
        /> -->

        <!-- <div>
            <button
                class="m-3 text-sm btn"
                :disabled="!name"
                @click="go"
            >
                Go
            </button>
        </div> -->
    </div>
</template>
