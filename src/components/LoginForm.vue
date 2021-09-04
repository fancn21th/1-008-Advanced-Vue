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
    <SwitchCheckbox id="rememberme" v-model="rememberme" />
    <!-- <SwitchCheckbox
      :value="rememberme"
      @input="
        newValue => {
          rememberme = newValue;
        }
      "
    /> -->
    <button type="submit">提交</button>
  </form>
</template>

<script>
import SwitchCheckbox from './SwitchCheckbox.vue';

export default {
  components: {
    SwitchCheckbox,
  },
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
