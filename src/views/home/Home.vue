<script setup>
    import Header from './Header.vue'
    import Nav from './Nav.vue'
    import Footer from './Footer.vue'
    import Menu from './Menu.vue'
</script>

<template>
    <div class="home-page">
        <Header></Header>
        <Nav></Nav>
        <main>
            <div class="menu-banner container">
                <Menu/>
            
            </div>

            <!-- 服务 -->
            <div class="sub">
                <div class="container">服务</div>
            </div>
        </main>
        
    </div>
</template>

<style>

.home-page{
    color: red;
}



.menu{
    height: 460px;
}
.sub{
    height: 170px;
}
</style>