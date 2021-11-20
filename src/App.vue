<template>
  <div id="app">
    <contact-list :data="contactList">
      <template slot-scope="props">
        <contact :imgUrl="props.contact.imageUrl">{{
          props.contact.name
        }}</contact>
      </template>
    </contact-list>
  </div>
</template>

<script>
import ContactList from './components/ContactList.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'App',
  components: {
    ContactList,
    Contact,
  },
  data() {
    return {
      contactList: [
        {
          id: 1,
          name: 'John Doe',
          imageUrl: 'avatar-1',
        },
        {
          id: 2,
          name: 'Joe Lin',
          imageUrl: 'avatar-2',
        },
      ],
    };
  },
};
</script>

<style src="./assets/css/app.css" />
