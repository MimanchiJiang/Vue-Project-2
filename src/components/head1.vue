<template>
  <div class="nav">
    <div>
      <el-menu
        class="el-menu-demo nav-pad"
        mode="horizontal"
        @select="handleSelect"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <router-link to="/"
          ><img src="../assets/lunbo/logo.png" alt="" class="logo"
        /></router-link>
        <router-link to="/"
          ><el-menu-item index="1">{{ home }}</el-menu-item></router-link
        >
        <!-- router-link to 表示要跳转到哪里 -->
        <router-link to="/dataprocess"
          ><el-menu-item index="2">{{ workplace }}</el-menu-item></router-link
        >
        <el-menu-item index="3">{{ history }}</el-menu-item>

        <el-input
          placeholder="请输入内容"
          prefix-icon="el-icon-search"
          class="ipt"
        >
        </el-input>

        <div class="login">
          <el-button type="text" class="login1" v-on:keyup.enter="success">{{
            login
          }}</el-button>
          <span class="xie">/</span>
          <el-button type="text" class="login1" @click="zhuce">{{
            registration
          }}</el-button>
        </div>
      </el-menu>
    </div>
    <div>
      <login v-if="see"></login>
    </div>
  </div>
</template>

<script>
import login from "@/components/homechild/login";
export default {
  data() {
    return {
      see: false,
      home: "首页",
      workplace: "工作台",
      history: "历史记录",
      registration: "注册",
      login: "登录",
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    zhuce() {
      this.see = !this.see;
    },
  },
  components: {
    login,
  },
};
</script>

<style>
body {
  margin: 0 0 0 0;
  background-color: #f5f5f5;
}
.login {
  float: right;
  margin-right: 30px;
  line-height: 60px;
}
.login1 {
  color: #ffffff;
}
.nav-pad {
  padding-left: 50px;
  border-bottom: none;
  background-color: rgba(0, 0, 0, 0.767);
}
.ipt {
  width: 300px;
  line-height: 60px;
  margin-left: 40px;
}
.xie {
  color: #ffffff;
}
.logo {
  width: 40px;
  height: 40px;
  float: left;
  margin-right: 60px;
  margin-top: 12px;
}
</style>
