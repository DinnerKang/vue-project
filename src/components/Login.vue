<template>
  <div id="login">

    <h1>Login</h1>
    
    <form>
      <div>
        <label for="user_id">ID</label>
        <input type="text" id="user_id">
      </div>
      <div>
          <label for="user_pwd">Password</label>
          <input type="password" id="user_pwd">
      </div>
      <div>
          <button>Login</button>
      </div>
    </form>

  </div>
</template>

<script>
export default {

};
</script>

<style scoped>
    #login{
        text-align: center;
    }
</style>
