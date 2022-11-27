<template>
  <div>
    <img src="/img/banner.jpg" class="cars-img mt-5 pt-2" />
    <div class="p-4">
      <h1 class="header text-center mt-3">All Cars</h1>
      <p class="text-secondary col-md-8 col-10 text-center ml-auto mr-auto">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro vero, ea
        voluptatem in aut quia hic nobis? Tempora tenetur, culpa et nam
        accusantium repellendus libero maiores voluptate laboriosam quo
        molestias. Lorem ipsum dolor sit, amet consectetur adipisicing elit.
        Eligendi tempore, molestiae quisquam officia est quasi maxime asperiores
        quaerat iste hic eum, eveniet perspiciatis alias ipsam totam ratione
        maiores nulla laudantium!
      </p>

      <CarCollection :cars="cars" class="m-2 m-md-0"/>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState(["popularCars", "largeCars", "smallCars"]),
  },

  data() {
    return {
      cars: [],
    };
  },
  mounted() {
    this.cars.push(...this.popularCars);
    this.cars.push(...this.largeCars);
    this.cars.push(...this.smallCars);
    console.log(this.cars);
  },
  head() {
    return {
      title: "All Cars",
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
.cars-img {
  width: 100%;
  height: 200px;
  filter: brightness(0.5);
}
</style>