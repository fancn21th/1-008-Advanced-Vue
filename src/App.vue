<template>
  <div id="app">
    <div class="card">
      <div class="container">
        from: <date-picker v-model="date" /> to: <date-picker v-model="date2" />
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from './components/DatePicker.vue';

export default {
  name: 'App',
  components: {
    DatePicker,
  },
  data() {
    return {
      date: '2021-10-01',
      date2: '2021-10-01',
    };
  },
};
</script>

<style src="./assets/css/app.css" />
