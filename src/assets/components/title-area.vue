<template>
  <div class="title-area px-4">

    <div class="row">
      <div class="col-12">
        <div class="breadcrumbs-area clearfix">
          <h4 class="page-title pull-left"> </h4>
          <ul class="breadcrumbs pull-left">
            <li><span>Dashboard</span></li>
          </ul>
        </div>
      </div>
    </div>

    <div class="row">
      <div  id='client' class="col-12 col-md-6 d-flex align-items-center flex-wrap">
        <h2>Bienvenido Juan Ramirez </h2>

        <div id='client-phone' class="form-group my-3">
          <label for="select-phone" class="form-label mr-3">Telefono</label>
          <select class="form-control-lg" id="select-phone">
            <option value="8297813995">829-781-3995</option>
          </select>
        </div>

      </div>

      <resume-navigation></resume-navigation>

    </div>
  </div>
</template>

<script>
  import ResumeNavigation from './resume-navigation.vue';
  export default {
    name: "title-area",
    components:{
      ResumeNavigation
    }
  }
</script>

<style scoped>

</style>
