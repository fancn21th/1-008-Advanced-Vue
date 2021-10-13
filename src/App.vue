<template>
  <div id="app">
    <!-- Trigger/Open The Modal -->
    <button @click="modalOpen = true">Open Modal</button>
    <modal :show="modalOpen" @close="modalOpen = false" />
  </div>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  components: {
    Modal,
  },
  data() {
    return {
      modalOpen: false,
    };
  },
};
</script>

<style src="./assets/css/app.css" />
