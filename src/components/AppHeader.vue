<template>
  <header>
    <!-- <h1>header logo</h1> -->
    <h1>{{propsdata}}</h1>
    <button v-on:click="sendEvent">send</button>
    <!-- 클릭시 일어날 이벤트를 메서드로 써준다 sendEvent와 메서드안의 sendEvent 명을 맞춰줌 -->
  </header>
</template>

<script>
export default {
    props: ['propsdata'],
    methods: {
        sendEvent: function () {  //이벤트 올려주기 renew이름으로
            this.$emit('renew'); // renew은 부모에 전달할 이벤트
        }
    }
}
</script>

<style>

</style>
<!-- 컴포넌트를 만들때 이름은 두단어 이상으로 조합하여
    단어 앞글자는 대문자로 생성한다 (소문자로 할경우 html 태그와 충돌할 수 있으므로)
    components안에 만들어준다
-->