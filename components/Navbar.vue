<template>
<div>
  <b-navbar toggleable="lg" type="light" variant="light" class="fixed-top pr-5 pl-5">
    <b-navbar-brand to="/#" class="navbar-brand">RENTY</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav class="justify-content-center">
      <b-navbar-nav>
        <b-nav-item to="/#" active>Home</b-nav-item>
        <b-nav-item to="/#about" active>About</b-nav-item>
        <b-nav-item href="/#services" active>Service</b-nav-item>
        <b-nav-item href="/#" active>Cars</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
      <div class="d-lg-block d-none">
        <button type="button" class="btn btn-dark">Download app</button>
      </div>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: "navbar"
    
};
</script>

<style>
.navbar-brand{
    font-weight: 700;
}
</style>