<template>
  <div>
    <h2 v-if="display">see</h2>
    <h2 v-show="display">see!</h2>
    <h2>{{ animals }}</h2>
    <h2 v-for="(animal,index) in animals" :key="index">
    <span v-if="animal !== 'rat'">{{ animal }} index : {{ index }}</span></h2>

    <h1>{{ cnt + 1 }}</h1>
    <button v-on:click="addNumber(1)">up</button>
    <h1>{{ cnt + 1 }}</h1>
    <button v-on:click="minNumber">down</button>
    <h1>{{ cnt + 1 }}</h1>
    <button v-on:mouseover="addNumber(10)">10up</button>



    <h2>{{ message }}</h2>
    <button @click="greeting">hi</button>
    <button @click="grreeting">bye</button>
    <div @click="getmousepo" class="box"></div>

    <button @click="addNumber($event,10)">10plus</button><button @click="addNumber($event,100)">100plus</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  methods: {
    getmousepo(event){
      console.log(event);
      this.message = `마우스의 위치는 ${event.pageX},${event.pageY}`;
    },
    greeting(){
      this.message = "hihi"
    },
    grreeting(){
      this.message = "byebye"
    },
    addNumber(event,value){
      this.message = `${event.pageX} adsa ${value}asd${event.pageX+value}`;
    },
    minNumber(){
      this.cnt = this.cnt - 1;
    },
},
  data(){
    return {
      cnt: 0,
      message: ""

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
button {
  width: 100px;
  height: 100px;
  font-size: 24px;
}
.box{
  width: 300px;
  height: 300px;
  background: #2c3e50;
}
</style>