<template>
  <div id="app">
    <router-view />

    <van-tabbar v-model="active">
      <van-tabbar-item icon="home-o" to='/'>首页</van-tabbar-item>
      <van-tabbar-item icon="search" to='/about'>发起</van-tabbar-item>
      <van-tabbar-item icon="setting-o" to='/'>标签</van-tabbar-item>
    </van-tabbar>

  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import { Icon, Tabbar, TabbarItem} from "vant";

@Component({
  components: {
    [Icon.name]:Icon,
    [Tabbar.name]:Tabbar,
    [TabbarItem.name]:TabbarItem
  }
})

export default class Apps extends Vue{
  active=0
    // icon= {
    //   active: 'https://img.yzcdn.cn/vant/user-active.png',
    //   inactive: 'https://img.yzcdn.cn/vant/user-inactive.png'
    // }

}

  
</script>

<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
</style>
