<template>
  <div id="app">
    <contact-list
      :data="contactList"
      :pseudo-slot="({ contact }) => contact.name"
    >
      <contact slot-scope="{ contact }" :imgUrl="contact.imageUrl">{{
        contact.name
      }}</contact>
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
