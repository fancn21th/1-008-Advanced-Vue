<template>
  <div id="app">
    <contact-modal-button></contact-modal-button>
  </div>
</template>

<script>
import ContactModalButton from './components/ContactModalButton.vue';

export default {
  name: 'App',
  components: {
    ContactModalButton,
  },
  data() {
    return {};
  },
};
</script>

<style src="./assets/css/app.css" />
