<template>
  <div>
    <el-dialog title="注册" :visible.sync="see">
      <el-form :model="user">
        <span class="lg_sp">用户名</span>
        <el-input v-model="user.name" placeholder="请输入用户名"></el-input>
        <span class="lg_sp">邮箱</span>
        <el-input v-model="user.email" placeholder="请输入电子邮箱"></el-input>
        <span class="lg_sp">密码</span>
        <el-input
          v-model="user.password"
          placeholder="请输入密码"
          type="password"
        ></el-input>
        <span class="lg_sp">确认密码</span>
        <el-input
          v-model="user.password1"
          placeholder="必须与上面密码一致"
          type="password"
          @keyup.enter="console.log('111')"
        ></el-input>
      </el-form>
      <div slot="footer" class="dialog-footer">
        <el-button @click="close">取 消</el-button>
        <el-button type="primary" @click="success">注册</el-button>
      </div>
    </el-dialog>
  </div>
</template>
<script>
export default {
  data() {
    return {
      see: true,
      user: {
        name: "",
        email: "",
        password: "",
        password1: "",
      },
      formLabelWidth: "80px",
    };
  },
  methods: {
    success() {
      console.log(this.user);
      window.alert(this.user.name + "欢迎");
      this.see = !this.see;
    },
    close() {
      this.see = !this.see;
    },
  },
};
</script>


<style>
.btn_h {
  position: absolute;
  left: 555px;
  top: 250px;
  width: 240px;
  height: 60px;
  border-radius: 10px;
  border: none;
  background-color: rgba(138, 138, 161, 0.6);
  font-size: 20px;
  color: white;
  cursor: pointer;
  letter-spacing: 5px;
  transition: 1s;
}
.btn_h:hover {
  background-color: rgba(138, 138, 161, 1);
}
.lg_sp {
  font-size: 15px;
}
</style>

