<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid d-flex">
      <nuxt-link class="navbar-brand" to="/">RENTY</nuxt-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-center" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/#about">About</nuxt-link>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Service</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Cars</a>
          </li>
        </ul>
      </div>

      <div>
        <button type="button" class="btn btn-dark">Download app</button>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navbar"
    
};
</script>

<style>
.navbar-brand{
    font-weight: 500;
}
</style>