<template>
  <div>
    {{ str }} {{ str2 }}
    <app-header></app-header>
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
      str2: 'hello?'
    }
  },
  components: {
    'app-header': AppHeader
  }
}
</script>

<style>

</style>