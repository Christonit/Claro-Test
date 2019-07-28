<template>
  <div class="col-12" :class="resolution.windowSize > resolution.xl ? 'col-lg-3':'col-lg-4'">


    <div class="vertical-cards ">

      <div class="w-100 d-flex align-items-center justify-content-between mb-1">
        <h6 class="ml-3">Mi factura</h6>

        <a href="#" class="btn btn-link">Histórico de pagos</a>

      </div>
      <div class="card card-report">
        <div class="card-info el-group">
          <div>
            <span class="card-label">Monto adeudado</span>
            <h5 class="report-value">$ 50,000</h5>
          </div>
          <a href="#" class="btn btn-primary">Pagar factura</a>
        </div>

        <div class="card-info mb-2">

          <span class="card-label">Fecha límite de pago </span>
          <h5 class="report-value">Julio 23, 2019</h5>
        </div>

        <hr>

        <div class="el-group mt-2 mb-2">

                    <span>
                      <span class="card-label">Plan</span>
                      <p class="black">Agosto 15, 2019</p>
                    </span>

          <span>
                      <span class="card-label">Días faltantes </span>
                      <p class="black">15</p>
                    </span>





        </div>

        <hr>


        <div class="el-group mt-2 mb-2">
          <a href="#" class="btn btn-outline-secondary">Descargar factura</a>
          <a href="#" class="btn btn-link-secondary">Ver factura</a>


        </div>


      </div>

    </div>

    <div class="vertical-cards">

      <div class="w-100 mb-3">
        <h6 class="ml-3">Mi cambiazo</h6>

      </div>
      <div class="card card-report">
        <div class="card-info el-group">
          <div>
            <span class="card-label">Aplicas para Cambiazo desde </span>
            <h5 class="report-value">Enero 1, 2019</h5>
          </div>
        </div>

        <div class="card-info mb-2">

          <span class="card-label">Ultima Fecha de Cambiazo</span>
          <h5 class="report-value">Marzo 13, 2019</h5>
        </div>



        <div class="el-group mt-2 mb-2 justify-content-between">

          <div class="w-50 has-border-right">
            <span class="card-label">último Cambiazo</span>
            <p class="black">Hace 4 meses</p>
          </div>

          <div class=" ">
            <span class="card-label">Próximo cambiazo</span>
            <p class="black">En 4 meses</p>
          </div>





        </div>


        <div class="el-group mt-2 mb-2 mt-3">
          <a href="#" class="btn btn-outline-primary mx-auto">Ver detalles</a>


        </div>


      </div>

    </div>


  </div>
</template>

<script>
    export default {
        name: "right-column",
      props:['resolution']
    }
</script>

<style scoped>

</style>
