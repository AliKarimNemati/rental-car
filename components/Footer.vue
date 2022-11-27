<template>
  <div>
    <div
      class="
        d-flex
        flex-wrap
        justify-content-center
        bg-dark
        text-white
        p-md-5 p-4
      "
    >
      <nuxt-link
        class="
          navbar-brand
          text-uppercase
          col-4
          text-md-start text-center text-light
        "
        to="/"
        >Renty</nuxt-link
      >
      <div
        class="
          col-md-3 col-12
          list-unstyled
          d-flex
          flex-wrap
          justify-content-center
          mt-3 mt-md-0
        "
      >
        <nuxt-link to="/" class="pr-3 text-light">Home</nuxt-link>
        <nuxt-link to="/#about" class="pr-3 text-light">About</nuxt-link>
        <nuxt-link to="/#services" class="pr-3 text-light">Service</nuxt-link>
        <nuxt-link to="/cars" class="pr-3 text-light">Cars</nuxt-link>
      </div>
      <div
        class="
          social-media
          col-md-4 col-12
          d-flex
          justify-md-content-end justify-content-center
          mt-3 mt-md-0
        "
      >
        <i class="bi bi-facebook"></i>
        <i class="bi bi-instagram"></i>
        <i class="bi bi-twitter"></i>
        <i class="bi bi-telegram"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.social-media i {
  font-size: 20px;
  width: 40px;
  height: 40px;
  padding: 4px;
  margin: 4px;
  border: 1px solid rgba(255, 255, 255, 0.426);
  border-radius: 50%;
  cursor: pointer;
  text-align: center;
}

.bi{
  transition: .5s;
}

.bi:hover{
  background: #eee;
  color: rgb(54, 116, 233);
  width: 45px;
  height: 45px;
  font-size: 24px;
}
</style>