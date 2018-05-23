<template>
	<div class="login-warp">
		<el-form label-width="80px" :model="userForm" label-position="top">
			<h4>用户登陆</h4>
			<el-form-item label="用户名">
				<el-input type="text" v-model="userForm.username"></el-input>
			</el-form-item>
			<el-form-item label="密码">
				<el-input type="password" v-model="userForm.password"></el-input>
			</el-form-item>
		<el-form-item>
			<el-button type="primary" class="logn-button" @click='login'>立即登陆</el-button>
			<!-- <el-button type="primary">取消</el-button> -->
		</el-form-item>
		</el-form>
	</div>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      userForm: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
    async login() {
      //  1、准备数据
      // console.log(this.userForm)

      // 2、发送请求

      // 3、根据相应做交互

      const res = await axios.post(
        "http://localhost:8888/api/private/v1/login",
        this.userForm
      );

      // console.log(res) 测试结果完成
      // console.log(res.data.meta)
      if (res.data.meta.status === 200) {
        this.$router.push({
          //编程式导航
          name: "home"
        });
      }
    }
  }
};
</script>

<style>
.login-warp {
  height: 100%;
  background: #324152;
  display: flex;
  justify-content: center;
	align-items: center;

}
.login-warp form{
		background:darkkhaki;
		padding: 30px;
		border-radius: 15px;
}
.logn-button{
	width:100%;
}
</style>