<template>
  <!-- 폼의 기본적인 동작을 막기 위한 modifier로써 흔히 사용하는 event.preventDefault()와 같은 효과 -->
  <form v-on:submit.prevent="submitForm">
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
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    submitForm: function() {
      //submit 태그 값을 전달하면 페이지 새로고침을 막는 메서드
      // event.preventDefault();
      
      console.log(this.username, this.password);

      var url = 'https://jsonplaceholder.typicode.com/users/';
      var data = {
        username: this.username,
        password: this.password
      };
      
      axios.post(url, data)
      .then(function(response) {
        console.log(response);
      })
      .catch(function(error) {
        console.log(error);
      })
    }
  }
}
</script>

<style>

</style>