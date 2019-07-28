<template>
  <div class="header-area w-100">
    <div class="row align-items-center">
      <!-- nav and search button -->
      <div class="col-md-6 col-sm-8 clearfix d-flex justify-content-start align-items-center">
          <h4>Mi Claro</h4>
        <div class="search-box ml-5">
          <form action="#">
            <i class="material-icons">
              search
            </i>
            <input type="text" name="Charch" placeholder="Buscar" required>

          </form>
        </div>
      </div>
      <!-- profile info & task notification -->
      <div class="col-md-6 col-sm-4 d-flex justify-content-end align-items-center">
        <a href="" class="btn btn-outline-secondary">Centros de atención</a>

          <a class=" dropdown-toggle" href="#" id="notif-dropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
<i class="sys-icon notification"> <span></span></i>
            <!--<div id="notification-center" class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">-->
              <!--<div class="notification-header"></div>-->
              <!--<div class="notification-content"></div>-->
            <!--</div>-->
          </a>
        
            <span class="profile-settings">
                <img src="../images/placeholder-img.png" alt="">
            </span>


      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "top-header"
    }
</script>

<style scoped>

</style>
