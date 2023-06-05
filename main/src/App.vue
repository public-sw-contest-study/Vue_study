<template>
  <div>
    <h3>당신의 나이는 {{age}}입니다.</h3>
    <h3 v-if="age > 18">당신은 어른입니다.</h3>
    <h3 v-else-if="age > 13 && age <= 18">당신은 청소년 입니다.</h3>
    <h3 v-else>당신은 어른이 아닙니다</h3>
    <!--if문 -->
    
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      age: 15
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>