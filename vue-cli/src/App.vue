<template>
  <div>
    {{ str }} {{ str2 }}
    <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
    <app-header v-bind:propsdata="headerStr"></app-header>
  </div>
</template>

<script>

import AppHeader from './components/AppHeader.vue';

// new Vue({
//   data: {
//     str: 'hi!',
//     str2: 'hello?'
//   }
// })

export default {
  name: 'app',
  data : function() {
    return {
      str: 'hi!',
      str2: 'hello?',
      headerStr: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  }
}
</script>

<style>

</style>