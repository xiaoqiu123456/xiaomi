
<script setup>
</script>

<template>
<header class="header">
    <div class="container">
        <div class="topbar-nav">
            <ul>
                <li>小米商城</li>
                <span class="sep">|</span>
                <li>MIUI</li>
                <span class="sep">|</span>
                <li>loT</li>
                <span class="sep">|</span>
                <li>云服务</li>
                <span class="sep">|</span>
                <li>天星舒克</li>
                <span class="sep">|</span>
                <li>有品</li>
                <span class="sep">|</span>
                <li>小米开放平台</li>
                <span class="sep">|</span>
                <li>企业团购</li>
                <span class="sep">|</span>
                <li>资质证照</li>
                <span class="sep">|</span>
                <li>协议规则</li>
                <span class="sep">|</span>
                <li>下载App</li>
                <span class="sep">|</span>
                <li>Select Location</li>
            </ul>
        </div>
        <div class="topbar-info">
            <div class="login">登录</div>
            <span class="sep">|</span>
            <div class="register">注册</div>
            <span class="sep">|</span>
            <div class="message">消息通知</div>
            <div class="shopping-cart">
                <span class="iconfont icon-gouwuche"></span>
                <p>购物车(0)</p>
            </div>
        </div>
    </div>
</header>
</template>

<style scoped>
    
/* 头部 */
.header{
    width: 100%;
    height: 40px;
    background-color: #333;
}
.topbar-nav{
    float: left;

}
.topbar-nav ul{
    display: flex;
}


.topbar-nav ul li, 
.register, 
.login,
.message{
    height: 40px;
    color: #b0b0b0;
    font-size: 12px;
    line-height: 40px;
    transition: color 0.3s;
}
.topbar-nav ul li:hover,
.register:hover, 
.login:hover,
.message:hover{
    color: #fff;
    cursor: pointer;
}
.sep{
    margin: 0 0.3em;
    color: #424242;
    line-height: 40px;
}

.topbar-info{
    float: right;
    display: flex;
}
.shopping-cart{
    width: 120px;
    margin-left: 12px;
    color: #b0b0b0;
    background: #424242;
    line-height: 40px;
    font-size: 12px;
    display: flex;
    transition: all 0.2s;
    justify-content: center;
}
.shopping-cart > p {
    margin-left: 4px;
}
.shopping-cart:hover{
    color: #ff6700;
    background-color: #fff;
    cursor: pointer;
}
</style>