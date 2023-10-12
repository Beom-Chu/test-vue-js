<template>
  <div>
    {{ str }} {{ str2 }}
  </div>
</template>

<script>

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
  }
}
</script>

<style>

</style>