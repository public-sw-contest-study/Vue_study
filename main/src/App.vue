<template>
  <div>
    <h1>hello {{ animal }}</h1>
    <h2>원숭이는 {{ food }}바나나를 좋아합니다.</h2>
    <h3 v-text="food"></h3>
    <input type="text" v-model="food" /><!--food라고 만들어둔 함수를 사용-->
    <div>{{ alertMessage }}</div>
    <div v-html="alertMessage"></div>
    <img v-bind:src="imageSource" alt="random" /><!--바인드 생략 가능 문법으로 만들때 사용-->
    <a :href="food">{{food}}</a>
    <hr />
    <h2 class="red">원숭이는 {{food}}를 좋아합니다</h2>
    <h2 v-bind:class="{ red: food==='apple',orange: food==='rice' }">원숭이는 {{food}}를 좋아합니다</h2><!--검색창에 애플이라고하면 바뀜-->

  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      animal: "Monkey",
      food: "banana",
      alertMessage: "<h2>rudrh!!!</h2>",
      imageSource: "https://placeimg.com/100/100/any",
      naverUrl: "https://www.naver.com",
    }
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
.orange {
  color: orange;
}
.red {
  color: red;
}
</style>