<template>
  <div id="app">
    <contact-list
      :data="contactList"
      :pseudo-slot="(props) => props.contact.name"
    >
      <contact slot-scope="props" :imgUrl="props.contact.imageUrl">{{
        props.contact.name
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
