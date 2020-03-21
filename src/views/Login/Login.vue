<template>
  <div class="login">
    <div class="top">
      <img src="@/components/img/logo01.png" alt="">
      <img src="@/components/img/logo.png" alt="" class="img">
    </div>
    <div class="nav">
      <van-tabs v-model="active">
        <van-tab title="Account login"><Accountlogin/></van-tab>
        <van-tab title="Code Logon">内容</van-tab>
      </van-tabs>
    </div>
    <div class="footer">
      注册
    </div>
  </div>
</template>

<style lang="scss" scoped>
.img{
  width: 124px;
  height: 124px;
  position: absolute;
  left: 120.5px;
  top: 56.5px;
}
.nav{
  margin-top: 77px;
}
</style>

<script>
import Vue from 'vue';
import { Tab, Tabs } from 'vant';
import Accountlogin from '@/views/Login/Accountlogin.vue'
Vue.use(Tab);
Vue.use(Tabs);
export default {
  name: 'login',
  data() {
    return {
      active: 2
    };
  },
  components: {
    Accountlogin
  }
}
</script>