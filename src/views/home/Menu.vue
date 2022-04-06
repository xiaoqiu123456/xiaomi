<script setup>
import { ref } from "@vue/reactivity";

    const current = ref(0);
    var menus = [
        {
            name: '手机',
            value: 1,
        },
        {
            name: '电视',
            value: 2,
        },
        {
            name: '笔记本 平板',
            value: 3,
        },
        {
            name: '家电',
            value: 4,
        },
        {
            name: '出行 穿戴',
            value: 5,
        },
        {
            name: '智能 路由器',
            value: 6,
        },
        {
            name: '电源 配饰',
            value: 7,
        },
        {
            name: '健康 儿童',
            value: 8,
        },
        {
            name: '耳机 音响',
            value: 9,
        },
        {
            name: '生活 箱包',
            value: 10,
        },
    ];
    // 鼠标移入
    var onMouseenter = function(menu) {
        // console.log('鼠标移入', menu)
        current.value = menu.value;
    }
    // 鼠标移出
    var onMouseout = function(menu) {
        // console.log('鼠标移出')
        current.value = 0;
    }
</script>

<template>
    <div class="menu">
        <ul>
            <li v-for="m in menus" :key="m.value" 
                :class="{'current': m.value === current}"
            
                @mouseenter="() => onMouseenter(m)"
                @mouseout="() => onMouseout(m)"
            >
                <a href="#">
                    <p class="name">{{m.name}}</p>
                    <span class="iconfont icon-gengduo icon"></span>
                </a>
            </li>
        </ul>
    </div>
</template>

<style scoped>
    .menu{
        width: 234px;
        height: 460px;
        padding: 20px 0;
        background: rgba(105, 101, 101, 0.6);
    }
    .menu ul{
        
    }
    .menu ul li{

    }
    .menu ul li a{
        color: #fff;
        padding-left: 30px;
        height: 42px;
        line-height: 42px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .menu .name{
        font-size: 14px;
    }
    .menu .icon{
        color: #e0e0e0;
        margin-right: 20px;
        font-size: 22px;
    }
    .current{
        transition: color .3s;
        background-color: #ff6700;
    }
</style>