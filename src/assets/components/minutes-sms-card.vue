<template>
  <div >
    <div class="card card-report">


      <div class="d-flex justify-content-around">
        <minutes-chart></minutes-chart>

        <sms-chart></sms-chart>

      </div>





    </div>
  </div>
</template>

<script>
  import MinutesChart from './minutes-chart.vue';
  import SmsChart from './sms-chart.vue';

  export default {
    name: "minutes-sms-card",
    data () {
      return {
        msg: 'Welcome to  Vue.js App'
      }
    },
    components: {
      MinutesChart,
      SmsChart
    }
  }

</script>

