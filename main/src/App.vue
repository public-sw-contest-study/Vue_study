<template>
  <div>
    <h2 v-if="display">see</h2>
    <h2 v-show="display">see!</h2>
    <h2>{{ animals }}</h2>
    <h2 v-for="(animal,index) in animals" :key="index">{{ animal }} index : {{ index }}</h2>

    <ul>
      <li v-for="(user,index) in users" :key="index">
        {{ user.name }}  {{ user.job }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      age: 15,
      display: false,
      animals: ["monkey","rat","dog","lion"],
      users: [
        {name: 'scalper', job: 'developer', gender:'male'},

        {name: 'jon', job: 'developer', gender:'male'},

        {name: 'asd', job: 'developer', gender:'male'},
      ]
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