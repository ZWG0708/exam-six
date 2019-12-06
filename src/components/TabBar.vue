<template>
    <div class="tab-bar">
        <router-link to="/home">首页</router-link>
        <router-link to="/about">我的</router-link>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
.tab-bar{
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    line-height: 50px;
    border-top: 1px solid #ccc;
    display: flex;
    a{
        flex: 1;
        text-align: center;
        text-decoration: none;
        &.router-link-active{
            color: greenyellow;
        }
    }
}
</style>