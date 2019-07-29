<template>
  <div class="title-area">

    <div class="row mb-3">
      <div class="col-12">
        <div class="breadcrumbs-area clearfix">
          <h4 class="page-title pull-left"> </h4>
          <ul class="breadcrumbs pull-left">
            <li><span>Resumen</span></li>
          </ul>
        </div>
      </div>
    </div>

    <div id='client' class="row">
      <div  :class="classPrint" class="col-12  d-flex align-items-center flex-wrap">
        <h2>Bienvenido <span class="red-highlight">Juan Ramírez</span></h2>

        <div id='client-phone' class="form-group my-3">
          <label for="select-phone" class="form-label mr-3">Teléfono</label>
          <select class="form-control-lg" id="select-phone">
            <option value="8297813995">829-781-3995</option>
          </select>
        </div>

      </div>

      <resume-navigation v-if="!isMobile" :class="resolution.windowSize <= resolution.xl ? 'col-md-6':'col-md-5'"></resume-navigation>

    </div>

    <hr >
  </div>
</template>

<script>
  import ResumeNavigation from './resume-navigation.vue';
  export default {
    name: "title-area",
    props:['resolution','isMobile'],
    components:{
      ResumeNavigation
    },computed:{

      classPrint(){
        if(this.resolution.windowSize <= this.resolution.lg){
          return '';
          // return this.resolution.windowSize;
        }

        if(this.resolution.windowSize <= this.resolution.xl){
          return 'col-md-6';
          // return this.resolution.windowSize;
        }

        if(this.resolution.windowSize > this.resolution.xl){
          return 'col-md-7';
          // return this.resolution.windowSize;
        }

      }
  }
  }
</script>
