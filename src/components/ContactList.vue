<template>
  <ul>
    <li v-for="contact in data" :key="contact.id">
      <slot :contact="contact">{{ contact.name }}</slot>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style></style>
