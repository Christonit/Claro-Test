<template>
  <div class="sidebar-menu">
    <div class="branding">
      <a href="index.html" class="d-flex justify-content-center"><img src="../images/claro-logo-d.svg" class='logo' alt="logo"></a>
    </div>
    <div >
      <div >
        <nav class="navbar navbar-expand-sm my-5">
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExample03" aria-controls="navbarsExample03" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>

          <div class="collapse navbar-collapse" id="navbarsExample03">
            <ul class="navbar-nav w-100">
              <li class="nav-item active">
                <a class="nav-link d-flex align-items-center" href="#"><i class="sys-icon  "></i> <span>Resumen</span> <span class="sr-only">(current)</span></a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Consultas</a>
              </li>

              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="https://example.com" id="dropdown03" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Administración</a>
                <div class="dropdown-menu" aria-labelledby="dropdown03">
                  <a class="dropdown-item" href="#">Action</a>
                  <a class="dropdown-item" href="#">Another action</a>
                  <a class="dropdown-item" href="#">Something else here</a>
                </div>
              </li>

              <li class="nav-item">
                <a class="nav-link" href="#">Pagos y recargas</a>
              </li>
            </ul>

          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "side-bar"
    }
</script>

