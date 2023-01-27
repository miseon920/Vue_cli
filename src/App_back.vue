<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <!--
    *컴포넌트 명명법 종류
    <hello-world></hello-world> 케밥으로 한 것이랑 위랑 같음
    <HelloWorld></HelloWorld> 카멜기법
    <HelloWorld />
  -->
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default { //new Vue() 와 같음
  //인스턴스 옵션속성 or 컴포넌트 옵션 속성
  name: 'App',
  components: {
    //HelloWorld // 'HelloWord': HelloWord 와 같음
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
