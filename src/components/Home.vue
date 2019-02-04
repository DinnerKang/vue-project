<template>
  <div id="home">
    <div>
      {{$store.state.id}}님 안녕하세요.
      여기는 홈 입니다.
      당신의 권환은 {{user_role}} 입니다.
    </div>
    <button v-on:click="goAdmin">ADMIN</button>
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
      if (this.user_role == "admin") {
        this.$router.push("/Admin");
      }
    }
  }
};
</script>


<style scoped>
</style>
