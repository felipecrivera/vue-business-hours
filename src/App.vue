<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <BusinessHours
        :days="demoHolidays"
        name="holidayHours"
        type="select"
        :time-increment="60"
        color="#00af0b"
      ></BusinessHours>
  </div>
</template>

<script>
import BusinessHours from './components/business-hours/components/BusinessHours.vue'
import demoDays from './data/demoDays';
import demoDaysSpanish from './data/demoDaysSpanish';
import demoHolidays from './data/demoHolidays';
import demoDaysErrors from './data/demoDaysErrors';
import demoSpanishLocalization from './data/demoSpanishLocalization';
import demoDaysEmit from './data/demoDaysEmit';

export default {
  name: 'App',
  components: {
    BusinessHours
  },
  data() {
    return {
      demoDays: demoDays,
      demoDaysSpanish: demoDaysSpanish,
      demoHolidays: demoHolidays,
      demoDaysErrors: demoDaysErrors,
      demoSpanishLocalization: demoSpanishLocalization,
      demoDaysEmit: demoDaysEmit
    };
  },
  methods: {
    updatedHours: function(val) {
      // eslint-disable-next-line
      console.log(val);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
