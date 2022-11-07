<template>
  <div>
    <Navbar />
    <HeroSection />
    <AboutUs />
    <Service />
    
  </div>
</template>

<script>
import HeroSection from "~/components/HeroSection.vue";
import Service from '~/components/Service.vue';
export default {
  components: { HeroSection, Service },
  name: "IndexPage",
};
</script>
