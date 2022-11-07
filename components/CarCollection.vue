<template>
  <div class="d-flex flex-wrap justify-content-center" v-if="isShow">
    <div
      class="card car-card border-top col-md-3 col-12 m-3 p-0"
      v-for="car in cars"
      :key="car.id"
    >
      <img
        :src="'img/' + car.img"
        class="card-img-top w-100"
        height="230"
      />
      <div class="card-body">
        <div class="d-flex justify-content-between">
          <h4 class="price">
            ${{ car.price }}
            <small class="text-secondary">/days</small>
          </h4>
          <small class="text-secondary">{{ car.loc }}</small>
        </div>
        <h5 class="card-title">{{ car.name }}</h5>
        <a href="#" class="btn btn-outline-dark">Booking Now</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:['cars', 'isShow']
};
</script>

<style>
</style>