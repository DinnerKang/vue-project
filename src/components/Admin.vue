<template>
  <div id="home">
    <div>
      안녕하세요
      여기는 어드민 페이지 입니다.
    </div>
    <div>
      <button class="btn" v-on:click="goHome">Home</button>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    this.$store.commit("userCheck");
  },
  methods: {
    goHome: function() {
      this.$router.push("/Home");
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
