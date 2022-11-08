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
      <h5 class="card-title">{{ car.name }}</h5>
      <b-button v-b-modal.rent-car-modal @click="handleCar" class="btn">Booking Now</b-button>
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