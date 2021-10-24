<template>
  <div id="app">
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

    <delete-modal
      :show="deleteModalOpen"
      @close="deleteModalOpen = false"
    ></delete-modal>
  </div>
</template>

<script>
import Modal from './components/Modal.vue';
import DeleteModal from './components/DeleteModal.vue';
import ContactForm from './components/ContactForm.vue';

export default {
  name: 'App',
  components: {
    Modal,
    ContactForm,
    DeleteModal,
  },
  data() {
    return {
      modalOpen: false,
      deleteModalOpen: false,
    };
  },
};
</script>

<style src="./assets/css/app.css" />
