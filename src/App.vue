<template>
  <div id="app">
    <div class="page-container">

      <side-bar :is-mobile="isMobile"></side-bar>

      <div class="main-content">

        <top-header></top-header>

        <resume-navigation v-if="isMobile" class="col-12"></resume-navigation>

        <title-area :is-mobile="isMobile" :resolution="resolution"></title-area>
        <div class="main-content-inner">

          <data-plan v-if="resolution.windowSize <= resolution.xl" :resolution="resolution" class="row"></data-plan>
          <div class="row">
            <data-plan  class="col-12 col-lg-3 px-0" :resolution='resolution' v-if="resolution.windowSize > resolution.xl"></data-plan>

            <data-usage-measurement  :class="isMobile ? 'mt-2':''" :resolution="resolution" :is-mobile="isMobile"></data-usage-measurement>


            <right-column :class="isMobile ? 'mt-4':''" :resolution="resolution"></right-column>
            <!-- overview area end -->





          </div>
        </div>

        <!-- footer area start-->
        <app-footer></app-footer>
        <!-- footer area end-->

      </div>

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

  window.onresize = function(){

    setTimeout( ()=>{
      location.reload();

    },2000)
  }

  export default {
    name: 'app',
    data () {
      return {
        resolution:{windowSize: screen.width,xs:512,sm:768,md:896,lg:1152,xmd:1280,xl:1440}
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

