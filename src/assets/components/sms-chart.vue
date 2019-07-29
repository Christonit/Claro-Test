<template>
  <div class="doughnut-chart-container d-flex align-content-center flex-wrap mb-2">

    <div class="doughnut-chart">
      <canvas ref="canvas"></canvas>
    </div>

    <span class="doughnut-chart-label">
          <h5 class="report-value">500</h5>
          <label>SMS</label>
        </span>

    <div class="card-label d-block w-100 text-center mt-2">Restantes <br> <mark class="black no-bg">125</mark></div>

  </div>
</template>

<script>
  import { Doughnut } from 'vue-chartjs'

  export default {
    name: "sms-chart",
    extends: Doughnut,
    data: () => ({
      chartdata: {
        labels: [ 'Disponibles','Consumidos'],
        datasets: [
          {
            // labels: ['Consumidos', 'Disponibles'],
            backgroundColor: ['#EFF0F0','#E42531'],
            data: [125, 375]
          }
        ],
      },
      options: {
        legend:{
          display:false
        },
        responsive: true,
        maintainAspectRatio: false,
        borderWidth:1,
        weight:1,

        cutoutPercentage:80
      }
    }),

    mounted () {
      this.renderChart(this.chartdata, this.options)
    }
  }
</script>
