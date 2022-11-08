<template>
  <div>
    <img :src="'img/' + car.img" class="card-img-top w-100" height="230" />
    <div class="card-body">
      <div class="d-flex justify-content-between">
        <h4 class="price">
          ${{ car.price }}
          <small class="text-secondary">/days</small>
        </h4>
        <small class="text-secondary">
          <i class="bi bi-geo-alt-fill"></i> {{ car.loc }}</small
        >
      </div>
      <nuxt-link class="card-title h5 text-dark" :to="'/cars/'+car.id">{{ car.name }}</nuxt-link>
      <b-button v-b-modal.rent-car-modal @click="handleCar" class="btn mt-3 col">Booking Now</b-button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["car"],
    methods:{
        handleCar(){
        this.$emit("getCar", this.car);
        }
    }
};
</script>

<style>
</style>