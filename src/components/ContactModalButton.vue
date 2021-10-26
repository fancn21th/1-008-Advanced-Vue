<template>
  <button @click="modalOpen = true">
    Open Modal

    <modal
      :show="modalOpen"
      :preventBackgroundSrolling="true"
      @close="modalOpen = false"
    >
      <contact-form @open:confirm-delete-modal="deleteModalOpen = true" />
    </modal>
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
