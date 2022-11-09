<template>
  <div class="mt-5 d-flex flex-wrap p-md-5 p-4 carDetail">
    <Modal :car="car" />

    <div class="col-md-5 col-12">
      <img :src="'../img/' + car.img" class="w-100 rounded" />
    </div>
    <div class="col-md-7 col-12">
      <h1 class="header">{{ car.name }}</h1>
      <p
        class="col-md-9 col-12 justify-md-content-center justify-content-start"
      >
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, sint
        officiis fugiat minima nobis quos distinctio. Deleniti eaque similique
        nisi facilis doloribus, magnam eius? Nihil cum et voluptate iusto.
        Aliquam?
      </p>
      <h2 class="pl-3 col-md-2 col-12">
        ${{ car.price }}<span class="text-secondary">/days</span>
      </h2>
      <span class="text-secondary pl-3">
        <i class="bi bi-geo-alt-fill"></i> {{ car.loc }}
      </span>
      <div>
        <b-button v-b-modal.rent-car-modal @click="handleCar" class="btn mt-4"
          >Booking Now</b-button
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      car: this.$store.getters.getCarsById(this.$route.params.id),
    };
  },
  methods: {
    handleCar() {
      this.$emit("getCar", this.car);
    },
  },
    head() {
    return {
      title: this.car.name,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Renty is the the best website for renting cars",
        },
      ],
    };
  },
};
</script>

<style>
span {
  font-size: 18px;
}
.carDetail {
  height: 75vh;
}
</style>