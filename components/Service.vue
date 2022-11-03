<template>
  <div id="services">
    <div class="bg-dark m-3 p-5">
      <p class="text-primary bold text-center">Our Services</p>
      <h1 class="header text-light col-5 text-center service-header">
        We have a best service for the rent cars
      </h1>
      <p class="text-secondary col-6 text-center service-info">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum pariatur
        rem perferendis fugiat deserunt natus praesentium officia quibusdam
        omnis.
      </p>
      <div class="d-flex cards">
        <div class="card col-3 m-3" v-for="(service, i) in services" :key="i">
          <div class="card-body">
            <h5 class="card-title text-center">{{service}}</h5>
            <p class="card-text text-center">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            services:['Quality Choice', 'Exclusive', 'Fast and Safe']
        }
    }
};
</script>

<style>
.service-header {
  margin: 0 auto;
}
.service-info {
  margin: 0 auto;
  margin-top: 16px;
}
.cards{
    justify-content: center;
    margin-top: 30px;
}

.card{
    border-top: #007bff 4px solid;
}
</style>