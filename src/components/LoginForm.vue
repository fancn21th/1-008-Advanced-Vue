<template>
  <form class="form-inline" @submit.prevent="submit">
    <label for="email">邮箱:</label>
    <input
      type="email"
      id="email"
      name="email"
      placeholder="Enter email"
      v-model="email"
    />
    <label for="pwd">密码:</label>
    <input
      type="password"
      id="pwd"
      name="pswd"
      placeholder="Enter password"
      v-model="pswd"
    />
    <!-- Rounded switch -->
    <label for="rememberme">记住我:</label>
    <label class="switch">
      <input
        type="checkbox"
        id="rememberme"
        name="rememberme"
        v-model="rememberme"
      />
      <span class="slider round"></span>
    </label>
    <button type="submit">提交</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      email: 'fancn21th@gmail.com',
      pswd: 'abcd',
      rememberme: false,
    };
  },
  methods: {
    submit() {
      console.log('表单提交内容', {
        email: this.email,
        pswd: this.pswd,
        rememberme: this.rememberme,
      });
    },
  },
};
</script>

<style></style>
