<template>
  <form class="form-inline" @submit.prevent="submit">
    <label for="email">邮箱:</label>
    <input
      type="email"
      id="email"
      placeholder="Enter email"
      name="email"
      v-model="email"
    />
    <label for="pwd">密码:</label>
    <input
      type="password"
      id="pwd"
      placeholder="Enter password"
      name="pswd"
      v-model="pswd"
    />
    <label> <input type="checkbox" name="remember" /> 记住我 </label>
    <button type="submit">提交</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      email: 'fancn21th@gmail.com',
      pswd: 'abcd',
    };
  },
  methods: {
    submit() {
      console.log('表单提交内容', {
        email: this.email,
        pswd: this.pswd,
      });
    },
  },
};
</script>

<style></style>
