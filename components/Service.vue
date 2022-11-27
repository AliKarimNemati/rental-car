<template>
  <div id="services">
    <div class="bg-dark m-3 p-md-5 p-4">
      <p class="text-primary bold text-center">Our Services</p>
      <h1 class="header text-light col-md-5 col-12 text-center service-header">
        We have a best service for the rent cars
      </h1>
      <p class="text-secondary col-md-6 col-12 text-center service-info">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum pariatur
        rem perferendis fugiat deserunt natus praesentium officia quibusdam
        omnis.
      </p>
      <div class="d-flex flex-wrap cards">
        <div class="card col-md-3 col-12 m-3" v-for="(service, i) in services" :key="i">
          <div class="card-body">
            <div class="text-center">
            <i class="bi bi-boxes service-icons"></i>
            </div>
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

.service-icons{
  font-size: 80px;
}
</style>