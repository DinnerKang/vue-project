<template>
  <div id="Login">
    <section>
      <article id="login_container">
        <div class="form_area">
          <form id="login_form">
            <div class="login_label">로그인</div>
            <div>
              <input class="login_input" type="text" placeholder="ID" id="user_id">
              <input class="login_input" type="password" placeholder="Password" id="user_pwd">
            </div>
            <div class="login_checkbox">
              <input type="checkbox"> 로그인 상태 유지
            </div>
            <div class="login_find">아이디 찾기 | 비밀번호 찾기</div>

            <div>
              <button id="login_btn" type="submit">로그인</button>
            </div>
          </form>
        </div>
      </article>
    </section>
  </div>
</template>


<script>
export default {};
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
    .login_label {
      font-size: 40px;
      color: $main_color;
      margin-bottom: 30px;
    }
    .login_input {
      width: 100%;
      height: 48px;
      margin-bottom: 16px;
      padding-left: 11px;
    }
    .login_checkbox {
      float: left;
    }
    .login_find {
      float: right;
    }
    #login_btn {
      margin-top:50px;
      color: #fff;
      width: 320px;
      height: 48px;
      border-radius: 23px;
      box-shadow: 0 4px 8px 0 #b4d7ff;
      background-color: #218aff;
      font-size: 13px;
    }
  }
}
</style>
