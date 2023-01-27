<template>
  <!-- 템플릿 아래 엘리먼트가 단 한개만 있어야함! 리액트와 다른점 <></> 은 쓸 수 없음 -->
  <div>
    <!-- {{str}} -->
    <!-- <AppHeader/> 3.사용하기 -->
    <!-- <AppHeader v-bind:프롭스속성이름="상위 컴포넌트에서 내릴 데이터 이름"/>  -->
    <AppHeader
     v-bind:propsdata="str"
     v-on:renew="renewStr"
    /> <!--하위컴포넌트에서 일어난 이벤트 renew 받고 실행할 이벤트 적어줌-->
  </div>
</template>

<script>

import AppHeader from './components/AppHeader.vue' //1.사용할 파일 import해주기 확장자인 .vue를 붙여줘야함

export default {
  /*
   data:{
    str:'hi'
   }
   cli에서는 재사용성으로 인하여 같은값을 다른곳에서 쓸수 있기 때문에 이렇게 쓸 수 없음
   아래의 형식으로 변경해서 써야함
   data: function () {  
      return {

      }
    }
   */
  data: function () {  
    return {
      //str: 'hi'
      str:'header props'
    }
  },
  components: { //2.components 에 사용할 컴포넌트 연결해 주기
    AppHeader
  },
  methods: {
    renewStr: function () { //적용할 이벤트
      this.str = 'hi vue'
    }
  }
}
</script>

<style>

</style>