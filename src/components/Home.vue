<template>
  <div id="home">
    <div>
      {{$store.state.id}}님 안녕하세요.
      여기는 홈 입니다.
      당신의 권환은 {{$store.state.role}} 입니다.
    </div>
    <button class="btn" v-on:click="goAdmin">Admin</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
  created() {
    this.$store.commit('userCheck');
  },
  methods: {
    goAdmin: function() {
      console.log("어드민으로 가기");
      if (this.$store.state.role == "admin") {
        this.$router.push("/Admin");
      }
    }
  }
};
</script>


<style scoped>
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
</style>
