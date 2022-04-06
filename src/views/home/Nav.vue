<script setup>
</script>

<template>
    <nav class="nav">
        <div class="container nav-box">
            <div class="header-logo">
                <a href="#">
                </a>
            </div>
            <div class="content">
                <ul>
                    <li>
                        <a class="link" href="#">Xiaomi手机</a>
                    </li>
                    <li>
                        <a class="link" href="#">Redmi红米</a>
                    </li>
                    <li>
                        <a class="link" href="#">电视</a>
                    </li>
                    <li>
                        <a class="link" href="#">笔记本</a>
                    </li>
                    <li>
                        <a class="link" href="#">平板</a>
                    </li>
                    <li>
                        <a class="link" href="#">家电</a>
                    </li>
                    <li>
                        <a class="link" href="#">路由器</a>
                    </li>
                    <li>
                        <a class="link" href="#">服务</a>
                    </li>
                    <li>
                        <a class="link" href="#">社区</a>
                    </li>
                </ul>
            </div>
            <div class="search">
                <input type="text" class="search-input" placeholder="小米手机"/>
                <div class="search-button">
                    <span class="iconfont icon-fangdajing"></span>
                </div>
            </div>
        </div>
    </nav>
</template>

<style scoped>
.nav-box{
    display: flex;
    height: 100px;
    justify-content: space-between;
    align-items:center;
}
.header-logo{
    width: 62px;
    margin-top: 22px;
}
.header-logo a{
    width: 56px;
    height: 56px;
    display: block;
    background-image: url('https://s02.mifile.cn/assets/static/image/logo-mi2.png');
    background-size:56px;
}
.content ul{
    display: flex;
    justify-content: center;
}
.content a{
    padding: 26px 10px;
    color: #333;
    line-height: 24px;
    font-size: 16px;
}
.search{
    display: flex;
}
.search:hover .search-input,
.search:hover .search-button{
    border-color: #666;
}
.search-input{
    border: 1px solid #e0e0e0;
    width: 225px;
    height: 50px;
    line-height: 50px;
    background-color: #fff;
    font-size: 14px;
    color: #333;
    padding: 0 10px;
    transition: all 0.3s;
}
.search-button{
    width: 50px;
    height: 50px;
    border: 1px solid #e0e0e0;
    border-left: 0px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 18px;
    color: #333;
    cursor: pointer;
    transition: all 0.3s;
}
.search-button:hover{
    color: #fff;
    background-color: #ff6700;

}
</style>