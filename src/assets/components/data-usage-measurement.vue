<template>
  <div class="col-12" :class="resolution.windowSize > resolution.xl ? 'col-lg-6':'col-lg-8'" >
    <div class=" col-12 w-100 d-flex align-items-center justify-content-between mb-3">
      <h6 class="">Medidor de uso</h6>

      <div>

        <label class="mr-2">Comparar</label>
        <label class="switch">
          <input type="checkbox">
          <span class="slider round"></span>
        </label>

      </div>


    </div>
    <div class="card data-usage-container">

      <div>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link active" data-toggle="tab" href="#home">Internet</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" data-toggle="tab" href="#menu1">Minutos</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" data-toggle="tab" href="#menu2">SMS</a>
          </li>
        </ul>

        <!-- Tab panes -->
        <div class="tab-content">
          <div id="home" class="container tab-pane active">
            <div class="el-group mb-4">

              <div class="form-group d-flex align-items-center options-input ">
                <label  class="">Fecha</label>
                <input type="date"  class="form-control">
              </div>




              <div class="el-group">

                <div class="form-group d-flex align-items-center options-input mr-4">
                  <label  class="">Filtrar</label>

                  <select class="form-control">
                    <option selected value="">Semana</option>
                    <option value="">Mes</option>
                    <option value="">Año</option>
                  </select>

                </div>

                <div class="btn-group btn-group-toggle toggle-icons" data-toggle="buttons">
                  <button type="button" class="btn active">
                    <i class="sys-icon bar-chart"></i>
                    <!--<input type="radio" name="options" id="option1" autocomplete="off" checked> Active-->
                  </button>
                  <button type="button" class="btn">
                    <i class="sys-icon line-chart"></i>
                  </button>

                </div>

              </div>


            </div>

            <data-usage-chart></data-usage-chart>


          </div>

          <div id="menu1" class="container tab-pane fade"><br>
            <h3>Menu 1</h3>
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
          </div>

          <div id="menu2" class="container tab-pane fade"><br>
            <h3>Menu 2</h3>
            <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
          </div>
        </div>
      </div>



      <div>
        <ul class="nav nav-tabs">

          <li class="nav-item">
            <a class="nav-link active" data-toggle="tab" href="#apps-plan">Apps incluidas</a>
          </li>

          <li class="nav-item">
            <a class="nav-link" data-toggle="tab" href="#my-apps">Mis apps</a>
          </li>
        </ul>

        <!-- Tab panes -->
        <div class="tab-content">

          <div id="apps-plan" class="container pt-2 tab-pane active">
            <div class="data-table">
              <div class="data-table-header">
                                <span class="cell w-80">
                                  Aplicación
                                </span>

                <span class="cell w-20 text-center">
                                  Uso
                                </span>

              </div>

              <div class="data-table-row">
                            <span class="cell w-60">
                              <i class="icon"><img src="../images/waze.png"></i>Waze
                            </span>

                <span class="cell w-20 text-center">
                              <span class="progress-bar">
                                <span class="progress-counter" style="width: 10%"></span>
                              </span>
                            </span>

                <span class="cell w-20 text-center">
                                200mb
                            </span>

              </div>


              <div class="data-table-row">
                            <span class="cell w-60">
                              <i class="icon"><img src="../images/instagram.png"></i>Instagram
                            </span>

                <span class="cell w-20 text-center">
                              <span class="progress-bar">
                                <span class="progress-counter" style="width: 40%"></span>
                              </span>
                            </span>

                <span class="cell w-20 text-center">
                                200mb
                            </span>

              </div>

              <div class="data-table-row">
                            <span class="cell w-60">
                              <i class="icon"><img src="../images/Whatsapp.png"></i>Whatsapp
                            </span>

                <span class="cell w-20 text-center">
                              <span class="progress-bar">
                                <span class="progress-counter" style="width: 50%"></span>
                              </span>
                            </span>

                <span class="cell w-20 text-center">
                                200mb
                            </span>

              </div>


              <div class="data-table-row">
                            <span class="cell w-60">
                              <i class="icon"><img src="../images/google-maps.png"></i>Google Maps
                            </span>

                <span class="cell w-20 text-center">
                              <span class="progress-bar">
                                <span class="progress-counter" style="width: 5%"></span>
                              </span>
                            </span>

                <span class="cell w-20 text-center">
                                200mb
                            </span>

              </div>

              <div class="data-table-row">
                            <span class="cell w-60">
                              <i class="icon"><img src="../images/twitter.png"></i>Twitter
                            </span>

                <span class="cell w-20 text-center">
                              <span class="progress-bar">
                                <span class="progress-counter" style="width: 15%"></span>
                              </span>
                            </span>

                <span class="cell w-20 text-center">
                                200mb
                            </span>

              </div>


            </div>

          </div>

          <div id="my-apps" class="container tab-pane fade"><br>
            <h3>Menu 2</h3>
            <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
          </div>
        </div>
      </div>






    </div>
  </div>
</template>



<script>
  import DataUsageChart from './data-usage-chart.vue';

  export default {
    name: "data-usage-measurement",
    props:['resolution','isMobile'],
      components:{
          DataUsageChart
      }
    }
</script>

<style scoped>

</style>
