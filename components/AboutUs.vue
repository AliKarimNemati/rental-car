<template>
  <div id="about">
    <div class="d-flex flex-wrap-reverse p-md-5 p-4">
      <div class="col-md-6 col-12 mt-3 mt-md-0">
        <img src="img/about us.jpg" class="w-100 rounded" />
      </div>

      <div class="col-md-5 m-md-4 p-md-4 col-12">
        <p class="text-primary bold">About Us</p>
        <h1 class="header">
          More than 150+ special collection cars
        </h1>
        <p class="text-muted">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempore
          necessitatibus quas aliquam nostrum, excepturi expedita id,
          consectetur molestias at ipsa, voluptatum soluta adipisci nam autem
          qui dignissimos!
        </p>
        <div>
          <nuxt-link to="/cars" class="btn btn-secondary">see all cars</nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
    .bold{
    font-weight: 600;
  }
</style>