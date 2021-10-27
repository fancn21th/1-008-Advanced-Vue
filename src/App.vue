<template>
  <div id="app">
    <contact-modal-button></contact-modal-button>

    <portal-target name="modals">
      <!--
      This component can be located anywhere in your App.
      The slot content of the above portal component will be rendered here.
      -->
    </portal-target>
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
