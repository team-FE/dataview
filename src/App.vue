<template>
  <div id="app">
    <!-- 路由 -->
    <transition name="router-fade" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>

<style lang="scss">
// 渐变动画
.router-fade-leave-active,
.router-fade-enter-active {
  transition: opacity 0.3s;
}
.router-fade-enter,
.router-fade-leave {
  opacity: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
