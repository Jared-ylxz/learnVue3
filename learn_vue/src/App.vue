<template>
  <el-container>
    <el-header>
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal"  :ellipsis="true" @select="handleSelect">
        <el-menu-item index="home">首页</el-menu-item>
        <el-menu-item index="currencyExchange">兑换货币</el-menu-item>
        <el-menu-item index="news">查看新闻</el-menu-item>
        <el-menu-item index="login">登录</el-menu-item>
        <el-menu-item index="register">注册</el-menu-item>
        <el-menu-item index="logout">退出</el-menu-item>
      </el-menu>
    </el-header>
    <el-main>
      <router-view></router-view>
    </el-main>
  <div id="app">
    <span>Count is: {{ count }}</span>
    <button @click="increment" :disabled="count >= 10">Plus</button>
    <button @click="decrease" :disabled="count <= 0">Minus</button>
    <div id="app2">
      <span>Message: {{ msg }}</span>
    </div>
    <div>
      <input v-model="msg" placeholder="edit me">
      <p>New message is: {{ msg }}</p>
    </div>
  </div>
  </el-container>
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

    function decrease() {
      count.value--;
      }

    return {
      count,
      msg,
      increment,
      decrease,
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
#app2 {
  color: royalblue;
}
</style>
