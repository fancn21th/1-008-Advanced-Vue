<template>
  <input :value="value" type="text" ref="input" placeholder="YYYY-MM-DD" />
</template>

<script>
import Pikaday from 'pikaday';
import '../../node_modules/pikaday/css/pikaday.css';

export default {
  props: {
    value: String,
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      format: 'YYYY-MM-DD',
      // toString(date) {
      //   const day = date.getDate();
      //   const month = date.getMonth() + 1;
      //   const year = date.getFullYear();
      //   return `${year}-${month}-${day}`;
      // },
      // parse(dateString) {
      //   const parts = dateString.split('-');
      //   const year = parseInt(parts[0], 10);
      //   const month = parseInt(parts[1], 10) - 1;
      //   const day = parseInt(parts[2], 10);
      //   return new Date(year, month, day);
      // },
      onSelect: () => {
        this.$emit('input', picker.toString());
      },
    });
  },
};
</script>

<style></style>
