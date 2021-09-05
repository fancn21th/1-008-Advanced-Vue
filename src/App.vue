<template>
  <div id="app">
    <div class="card">
      <div class="container">
        <input :value="date" type="text" ref="input" placeholder="YYYY-MM-DD" />
      </div>
    </div>
  </div>
</template>

<script>
import Pikaday from 'pikaday';
import '../node_modules/pikaday/css/pikaday.css';

export default {
  name: 'App',
  components: {},
  data() {
    return {
      date: '2021-10-01',
    };
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      format: 'D/M/YYYY',
      toString(date) {
        const day = date.getDate();
        const month = date.getMonth() + 1;
        const year = date.getFullYear();
        return `${year}-${month}-${day}`;
      },
      parse(dateString) {
        const parts = dateString.split('-');
        const year = parseInt(parts[0], 10);
        const month = parseInt(parts[1], 10) - 1;
        const day = parseInt(parts[2], 10);
        return new Date(year, month, day);
      },
      onSelect: () => {
        this.date = picker.toString();
      },
    });
  },
};
</script>

<style src="./assets/css/app.css" />
