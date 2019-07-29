<template>
  <div class="data-plan ">
    <div class=" col-12 w-100 d-flex align-items-center justify-content-between mb-3">
      <h6 class="ml-3">Datos del plan</h6>

    </div>
    <div class=" col-12" :class="resolution.windowSize <= resolution.xl ?'col-md-4': ''">
      <div class="card card-report">

        <div class="card-info">
          <span class="card-label">Plan</span>
          <h5 class="report-value">Smart Postpago 100</h5>
        </div>

        <div class="card-info">
          <span class="card-label">Estado</span>

          <div class="el-group">
            <span class="badge status-success">Activo</span>

            <a href="#" class="btn btn-link">Ver detalles</a>
          </div>

        </div>

        <span class="disclaimer">*Servicio factura el día 22 de cada mes.</span>
      </div>
    </div>


    <div class="col-12" :class="resolution.windowSize <= resolution.xl ?'col-md-4': ''">
      <div class="card card-report">

        <div class="card-info el-group">

          <div>

            <span class="card-label">Internet</span>
            <h5 class="report-value">1GB</h5>

          </div>


          <a href="#" class="btn btn-outline-primary">Comprar paquetico</a>




        </div>

        <div class="card-info mt-2">
                    <span class="progress-bar">
                      <span class="progress-counter" style="width: 60%"></span>
                    </span>

          <div class="el-group mt-2">
            <span class="card-label">Consumido <br> <mark class="black no-bg">900 mb</mark></span>



            <span class="card-label text-right">Restante<br><mark class="black no-bg p-0">100 mb</mark></span>


          </div>







        </div>

        <div class="el-group mt-1">
          <span class="card-label text-right">Total <mark class="black no-bg p-0">1GB</mark></span>

          <span class="disclaimer">*Total incluyendo rollover.</span>

        </div>

      </div>
    </div>


    <minutes-sms-card class="col-12" :class="resolution.windowSize <= resolution.xl ?'col-md-4': ''"></minutes-sms-card>



  </div>
</template>

<script>
  import MinutesSmsCard from './minutes-sms-card.vue';
  import DataUsageChart from './data-usage-chart.vue';

  export default {
    name: "data-plan",
    props:['resolution'],
    components:{
      MinutesSmsCard,
      DataUsageChart

    }
  }
</script>

