<template>
  <div id="Login">
    <section>
      <article id="login_container" v-if="isLogin">
        <div class="form_area">
          <form id="login_form" v-on:submit.prevent="loginSubmit">
            <div class="label">로그인</div>
            <div>
              <input
                class="login_input"
                type="text"
                placeholder="ID"
                id="user_id"
                v-model="user_id"
              >
              <input
                class="login_input"
                type="password"
                placeholder="Password"
                id="user_pwd"
                v-model="user_pwd"
              >
            </div>
            <button type="button" class="btn_small" v-on:click="registBtn()">회원가입</button>
            <div>
              <button class="btn" id="login_btn" type="submit">로그인</button>
            </div>
          </form>
        </div>
      </article>
      <article id="register_container" v-if="isRegister">
        <div class="register_box">
          <form id="register_form" v-on:submit.prevent="registerSubmit">
            <div class="label">회원가입</div>
            <div>
              <input
                class="login_input"
                type="text"
                placeholder="ID"
                id="register_id"
                v-model="register_id"
              >
              <input
                class="login_input"
                type="password"
                placeholder="Password"
                id="register_pwd"
                v-model="register_pwd"
              >
              <select id="user_role" v-model="register_role">
                <option value="Admin">Admin</option>
                <option value="User">User</option>
              </select>
              <button class="btn_small" type="button" v-on:click="cancelBtn">취소</button>
            </div>
            <div>
              <button class="btn" type="submit">회원가입</button>
            </div>
          </form>
        </div>
      </article>
    </section>
  </div>
</template>


<script>
export default {
  data() {
    return {
      user_id: "",
      user_pwd: "",
      isLogin: true,
      isRegister: false,
      register_id: "",
      register_pwd: "",
      register_role: "Admin"
    };
  },
  methods: {
    loginSubmit: function() {
      console.log("로그인");
      this.$Axios.post(`$`)
      this.$router.push("/");
    },
    showLogin: function() {
      this.isLogin = true;
      this.isRegister = false;
    },
    showRegister: function() {
      this.isLogin = false;
      this.isRegister = true;
    },
    registerSubmit: function() {
      console.log("회원가입 완료");
      this.showLogin();
    },
    registBtn: function() {
      console.log("회원가입");
      this.showRegister();
    },
    cancelBtn: function() {
      this.showLogin();
    }
  }
};
</script>


<style lang="scss" scoped>
$main_color: #4c84ff;

#login_container {
  float: right;
  text-align: center;
  height: 100vh;
  width: 100%;
  box-sizing: border-box;
  position: relative;
  .form_area {
    width: 100%;
    height: 440px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    #login_form {
      width: 320px;
      height: 440px;
      margin: 0 auto;
    }
    .login_checkbox {
      float: left;
      font-size: 13px;
    }
    .login_find {
      float: right;
      font-size: 13px;
    }
  }
}
#register_container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  width: 100%;
  position: absolute;
  top: 0;
  .register_box {
    width: 320px;
    height: 440px;
    background: #fff;
  }
}
.btn {
  margin-top: 50px;
  color: #fff;
  width: 320px;
  height: 48px;
  border-radius: 23px;
  box-shadow: 0 4px 8px 0 #b4d7ff;
  background-color: #218aff;
  font-size: 13px;
  border: none;
  cursor: pointer;
}
.btn_small {
  float: right;
  color: #fff;
  width: 80px;
  height: 24px;
  box-shadow: 0 4px 8px 0 #b4d7ff;
  background-color: #218aff;
  font-size: 11px;
  border: none;
  cursor: pointer;
}
.label {
  text-align: center;
  font-size: 40px;
  color: $main_color;
  margin-bottom: 30px;
}
#user_role {
  height: 25px;
  float: left;
}
.login_input {
  width: 100%;
  height: 48px;
  margin-bottom: 16px;
  padding-left: 11px;
  box-sizing: border-box;
}
</style>
