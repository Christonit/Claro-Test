<template>
  <div id="app">
    <div class="page-container">
      <!-- sidebar menu area start -->
      <side-bar></side-bar>
      <!-- sidebar menu area end -->
      <!-- main content area start -->
      <div class="main-content">
        <!-- header area start -->
        <top-header></top-header>
        <!-- header area end -->
        <!-- page title area start -->
              <title-area :resolution="resolution"></title-area>
        <!-- page title area end -->
        <div class="main-content-inner">
          <!-- sales report area start -->
            <data-plan v-if="resolution.windowSize <= resolution.xl" :resolution="resolution" class="row"></data-plan>
          <!-- sales report area end -->
          <!-- overview area start -->
          <div class="row">
            <data-plan  class="col-lg-3 px-0" :resolution='resolution' v-if="resolution.windowSize > resolution.xl"></data-plan>

            <div class="col-12" :class="resolution.windowSize > resolution.xl ? 'col-lg-6':'col-lg-8'" >
              <div class=" col-12 w-100 d-flex align-items-center justify-content-between mb-3">
                <h6 class="ml-2">Medidor de uso</h6>

                <div>

                  <label class="mr-2">Comparar</label>
                  <label class="switch">
                    <input type="checkbox">
                    <span class="slider round"></span>
                  </label>

                </div>


              </div>
              <div class="card">

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
                              <i class="icon"><img src="./assets/images/waze.png"></i>Waze
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
                              <i class="icon"><img src="./assets/images/instagram.png"></i>Instagram
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
                              <i class="icon"><img src="./assets/images/Whatsapp.png"></i>Whatsapp
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
                              <i class="icon"><img src="./assets/images/google-maps.png"></i>Google Maps
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
                              <i class="icon"><img src="./assets/images/twitter.png"></i>Twitter
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


            <right-column :resolution="resolution"></right-column>
          <!-- overview area end -->
          <!-- market value area start -->


        </div>
      </div>
      <!-- main content area end -->
      <!-- footer area start-->
      <footer>
        <div class="footer-area">
          <p>© Copyright 2018. All right reserved. Template by <a href="https://colorlib.com/wp/">Colorlib</a>.</p>
        </div>
      </footer>
      <!-- footer area end-->
    </div>
    <!-- page container area end -->
    <!-- offset area start -->

  </div>

    <a href="#" id="chat-cta" class="btn btn-lg"> <i class="chat-icon"></i> <span><b>Chat Claro </b><br>Necesita ayuda?</span></a>

  </div>

  </div>
</template>

<script>
  import SideBar from './assets/components/side-bar.vue';
  import TopHeader from './assets/components/top-header.vue';
  import TitleArea from './assets/components/title-area.vue';
  import DataPlan from './assets/components/data-plan.vue';
  import RightColumn from './assets/components/right-column.vue';
  import DataUsageChart from './assets/components/data-usage-chart.vue';


export default {
  name: 'app',
  data () {
    return {
      resolution:{windowSize: window.innerWidth,xs:512,sm:768,md:896,lg:1152,xl:1440}
    }
  },
  components:{
    SideBar,
    TopHeader,
    TitleArea,
    DataPlan,
    RightColumn,
    DataUsageChart
  }
}
</script>

<style lang="scss">

  @import "./assets/scss/style.scss";
</style>
