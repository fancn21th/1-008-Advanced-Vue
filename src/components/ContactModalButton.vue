<template>
  <button @click="modalOpen = true" style="opacity: .5">
    Open Modal
    <modal
      :show="modalOpen"
      :preventBackgroundSrolling="true"
      @close="modalOpen = false"
    >
      <contact-form />
    </modal>
    <portal to="modals" v-if="modalOpen"> </portal>
  </button>
</template>

<script>
import Modal from './Modal.vue';
import ContactForm from './ContactForm.vue';

export default {
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

<style></style>
