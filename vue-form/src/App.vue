<template>
  <form v-on:submit="submitForm">
    <div>
      <label for="username">id : </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw : </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
export default {
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    submitForm: function(event) {
      //submit 태그 값을 전달하면 페이지 새로고침을 막는 메서드
      event.preventDefault();
      
      console.log(this.username, this.password);
    }
  }
}
</script>

<style>

</style>