<template>
  <button @click="deleteModalOpen = true" class="deleteBtn">
    Delete

    <delete-modal
      :show="deleteModalOpen"
      @close="deleteModalOpen = false"
    ></delete-modal>
  </button>
</template>

<script>
import DeleteModal from './DeleteModal.vue';

export default {
  components: {
    DeleteModal,
  },
  data() {
    return {
      deleteModalOpen: false,
    };
  },
};
</script>

<style>
.deleteBtn {
  background: #f50000;
}
</style>
