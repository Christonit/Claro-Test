<template>
  <div class="header-area w-100">
    <div class="row align-items-center">
      <!-- nav and search button -->
      <!--<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#main-menu" aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">-->
        <!--<span class="navbar-toggler-icon"></span>-->
      <!--</button>-->

      <div class="col-2 d-block d-sm-none">
        <div class="nav-btn ">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div class="col-6 col-md-7 col-sm-8 clearfix d-flex justify-content-start align-items-center">
          <h4 class="d-none d-md-block">Mi Claro</h4>
          <div class="mobile-logo d-block d-sm-none"><img src="../images/claro-logo-m.svg" alt=""></div>
        <div class="search-box ml-5 d-none d-sm-block">
          <form action="#">
            <i class="material-icons">
              search
            </i>
            <input type="text" name="Charch" placeholder="Buscar" required>

          </form>
        </div>
      </div>
      <!-- profile info & task notification -->
      <div class="col-4 col-md-5 d-flex justify-content-end align-items-center">
        <a href="" class="btn btn-outline-secondary d-none d-md-block">Centros de atención</a>

          <a class=" dropdown-togg le" href="#" id="notif-dropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
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
