<template>
  <div id="app">
    <contact-list :data="contactList"></contact-list>
  </div>
</template>

<script>
import ContactList from './components/ContactList.vue';

export default {
  name: 'App',
  components: {
    ContactList,
  },
  data() {
    return {
      contactList: [
        {
          id: 1,
          name: 'John Doe',
        },
        {
          id: 2,
          name: 'Joe Lin',
        },
      ],
    };
  },
};
</script>

<style src="./assets/css/app.css" />
