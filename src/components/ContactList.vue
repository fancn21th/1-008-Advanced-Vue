<template>
  <ul>
    <li v-for="contact in data" :key="contact.id">
      <slot :contact="contact">{{ contact.name }}</slot>
      {{ pseudoSlot({ contact: contact }) }}
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
    pseudoSlot: {
      type: Function,
      default: () => null,
    },
  },
};
</script>

<style></style>
