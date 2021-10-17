<template>
  <div id="app">
    <button @click="modalOpen = true">Open Modal</button>
    <modal
      :show="modalOpen"
      :preventBackgroundSrolling="true"
      @close="modalOpen = false"
    >
      <contact-form />
    </modal>
  </div>
</template>

<script>
import Modal from './components/Modal.vue';
import ContactForm from './components/ContactForm.vue';

export default {
  name: 'App',
  components: {
    Modal,
    ContactForm,
  },
  data() {
    return {
      modalOpen: false,
    };
  },
};
</script>

<style src="./assets/css/app.css" />
