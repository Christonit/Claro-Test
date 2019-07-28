<template>
    <div>
      <canvas class='usage-chart' ref="canvas"></canvas>
    </div>
</template>

<script>
  import { Line } from 'vue-chartjs'

  export default {
    name: "data-usage-chart",
    extends: Line,
    data: () => ({
      chartdata: {
        labels: [ '24 Jun - 30 jun','1 jul - 7 jul','8 jul - 14 jul','15 jul - 21 jul','22 jul - 28 jul'],
        datasets: [
          {
            label: 'Actual',
            backgroundColor: ['#EFF0F0','#E42531'],
            data: [250, 50,150,500,20],
            lineTension:0,
            borderColor:'#27BCD8',
            backgroundColor:'rgba(0, 0, 0, 0)',
            pointBorderColor:'#ffffff',
            pointRadius:5,
            pointHitRadius:12,
            pointBackgroundColor:'#27BCD8',
            pointBorderWidth:2,



          }
        ],
      },
      options: {
        legend:{
          labels:{
            defaultFontColor:'#B4B9BB',
            defaultFontFamily:'Roboto, sans-serif',
            defaultFontSize:10,
            padding:12


          },
          display:false,
          position:'bottom',
        },
        responsive: true,
        maintainAspectRatio: false
      }
    }),

    mounted () {
      this.renderChart(this.chartdata, this.options)
    }
  }
</script>

<style scoped>

</style>
