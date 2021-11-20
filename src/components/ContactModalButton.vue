<template>
  <button @click="modalOpen = true">
    Open Modal
    <modal-dialog
      :show="modalOpen"
      :preventBackgroundSrolling="true"
      @close="modalOpen = false"
    >
      <contact-form />
    </modal-dialog>
  </button>
</template>

<script>
import ModalDialog from './ModalDialog.vue';
import ContactForm from './ContactForm.vue';

export default {
  components: {
    ModalDialog,
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
