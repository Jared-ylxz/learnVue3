<template>
  <!-- <el-container>
    <el-header>
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal"  :ellipsis="true" @select="handleSelect">
        <el-menu-item index="home">首页</el-menu-item>
        <el-menu-item index="currencyExchange">兑换货币</el-menu-item>
        <el-menu-item index="news">查看新闻</el-menu-item>
        <el-menu-item index="login" v-if="!authStore.isAuthenticated">登录</el-menu-item>
        <el-menu-item index="login">登录</el-menu-item>
        <el-menu-item index="register">注册</el-menu-item>
        <el-menu-item index="logout">退出</el-menu-item>
      </el-menu>
    </el-header>
    <el-main>
      <router-view></router-view>
    </el-main>
  </el-container> -->
  <div id="app">
    <button @click="increment">
      Count is: {{ count }}
    </button>
    <div>
      <span>Message: {{ msg }}</span>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const count = ref(0);
    var msg = 'Hello Vue 3.0!';

    function increment() {
      count.value++;
      }

    return {
      count,
      msg,
      increment,
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
