<template>
  <div id="collection">
    <div class="p-md-5 p-4">
      <p class="text-primary bold text-center">Collection</p>
      <h1 class="header text-center">Our Collection Cars</h1>
      <div class="mt-3">
        <ul
          class="
            d-flex
            justify-content-around
            border-bottom
            text-secondary
            list-unstyled
          "
        >
          <li
            class="p-3 element"
            :class="{ selected: popularCarsShow }"
            @click="handleElements('p')"
          >
            Popular
          </li>
          <li
            class="p-3 element"
            :class="{ selected: largeCarsShow }"
            @click="handleElements('l')"
          >
            Large Cars
          </li>
          <li
            class="p-3 element"
            :class="{ selected: smallCarsShow }"
            @click="handleElements('s')"
          >
            Small Cars
          </li>
        </ul>
      </div>

        <CarCollection :cars="popularCars" :isShow="popularCarsShow" />
        <CarCollection :cars="largeCars" :isShow="largeCarsShow" />
        <CarCollection :cars="smallCars" :isShow="smallCarsShow" />

      <div class="text-center">
        <nuxt-link to="/cars" class="btn btn-primary">see all cars</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  data() {
    return {
      largeCarsShow: false,
      smallCarsShow: false,
      popularCarsShow: true,
    };
  },
  computed: {
    ...mapState(["popularCars", "largeCars", "smallCars"]),
  },
  methods: {
    handleElements(key) {
      if (key == "p") {
        this.smallCarsShow = false;
        this.largeCarsShow = false;
        this.popularCarsShow = true;
      } else if (key == "l") {
        this.smallCarsShow = false;
        this.popularCarsShow = false;
        this.largeCarsShow = true;
      } else if (key == "s") {
        this.popularCarsShow = false;
        this.largeCarsShow = false;
        this.smallCarsShow = true;
      }
    },
  },
};
</script>

<style>
.selected {
  border-bottom: 2px solid black !important;
}

.element {
  cursor: pointer;
}

.car-card {
  border-top: 0;
}
.price {
  font-weight: 700;
}
small {
  font-size: 16px;
}
</style>