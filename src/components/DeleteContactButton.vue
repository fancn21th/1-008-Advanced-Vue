<template>
  <button @click="deleteModalOpen = true" class="deleteBtn">
    Delete
    <modal-dialog
      :show="deleteModalOpen"
      :preventBackgroundSrolling="true"
      @close="deleteModalOpen = false"
    >
      <!-- 自定义 删除 Dialog  TODO: 可以封装成一个单独的组件 -->
      <div class="container">
        <h1>Delete Account</h1>
        <p>Are you sure you want to delete your account?</p>

        <div class="clearfix">
          <button
            type="button"
            class="cancelbtn"
            @click.stop="deleteModalOpen = false"
          >
            Cancel
          </button>
          <button type="button" class="deletebtn">
            Delete
          </button>
        </div>
      </div>
    </modal-dialog>
  </button>
</template>

<script>
import ModalDialog from './ModalDialog.vue';

export default {
  components: {
    ModalDialog,
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
