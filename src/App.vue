<template>
  <div id="app">
    <div class="page-container">
      <!-- sidebar menu area start -->
      <side-bar :is-mobile="isMobile"></side-bar>
      <!-- sidebar menu area end -->
      <!-- main content area start -->
      <div class="main-content">
        <!-- header area start -->
        <top-header></top-header>

        <!--<div class="row">-->
          <resume-navigation v-if="isMobile" class="col-12"></resume-navigation>
        <!--</div>-->

        <!-- header area end -->
        <!-- page title area start -->
              <title-area :is-mobile="isMobile" :resolution="resolution"></title-area>
        <!-- page title area end -->
        <div class="main-content-inner">
          <!-- sales report area start -->
            <data-plan v-if="resolution.windowSize <= resolution.xl" :resolution="resolution" class="row"></data-plan>
          <!-- sales report area end -->
          <!-- overview area start -->
          <div class="row">
            <data-plan  class="col-12 col-lg-3 px-0" :resolution='resolution' v-if="resolution.windowSize > resolution.xl"></data-plan>

            <data-usage-measurement :resolution="resolution" :is-mobile="isMobile"></data-usage-measurement>


            <right-column :resolution="resolution"></right-column>
          <!-- overview area end -->
          <!-- market value area start -->


        </div>
      </div>
      <!-- main content area end -->
      <!-- footer area start-->
      <app-footer></app-footer>
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
  import AppFooter from './assets/components/app-footer.vue';
  import TopHeader from './assets/components/top-header.vue';
  import TitleArea from './assets/components/title-area.vue';
  import DataPlan from './assets/components/data-plan.vue';
  import DataUsageMeasurement from './assets/components/data-usage-measurement.vue';
  import RightColumn from './assets/components/right-column.vue';
  import ResumeNavigation from './assets/components/resume-navigation.vue';


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
    ResumeNavigation,
    TitleArea,
    DataPlan,
    RightColumn,
    DataUsageMeasurement,
    AppFooter
  },computed:{
    isMobile(){
      return this.resolution.windowSize <= this.resolution.sm;
    }
  },
}
</script>

<style lang="scss">

  @import "./assets/scss/style.scss";
</style>
