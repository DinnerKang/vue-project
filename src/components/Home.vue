<template>
    <div id="home">
        <div>
          {{user_id}}님 안녕하세요.

          여기는 홈 입니다.
            당신의 권환은 {{user_role}} 입니다.
        </div>
        <button v-on:click="goAdmin">ADMIN</button>
    </div>
</template>

<script>
export default {
    data(){
        return{
            user_id = '',
            user_role='',

        }
    },
    methods:{
        goAdmin : function () {
            console.log('어드민으로 가기');
            this.$router.push('/Admin');
        }
    }
}
</script>


<style scoped>

</style>
