<template>
  <div>
    <div class="d-flex p-5">
      <div class="col-md-5 col-12">
        <h1 class="header">
          Search and find your best car rental with easy way
        </h1>
        <p class="text-muted">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempore
          necessitatibus quas aliquam nostrum, excepturi expedita id,
          consectetur molestias at ipsa, voluptatum soluta adipisci nam autem
          qui dignissimos!
        </p>
        <div>
          <button type="button" class="btn btn-primary">Booking now</button>
          <nuxt-link to="/" class="p-3 text-dark h5">see all cars</nuxt-link>
        </div>
      </div>

      <div class="col-md-7 col-12">
        <img src="img/maserati ghibli 2021.jpg" class="w-100 rounded" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
};
</script>

<style>
.header {
  font-weight: 700;
  font-size: 3rem;
}
</style>