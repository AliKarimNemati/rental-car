<template>
  <div class="d-flex flex-wrap justify-content-center"  >
    <Modal :car="car"/>
    <Card class="card car-card border-top col-md-3 col-12 m-3 p-0" v-for="car in
    cars" :key="car.id" :car="car" @getCar="getCar"/>
  </div>
</template>

<script>
export default {
  props: ["cars"],
  data(){
    return{
      car:{}
    }
  },
  methods:{
    getCar(e){
      this.car = e;
    }
  }
};
</script>

<style>
</style>