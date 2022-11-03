<template>
  <div>
    <Navbar />
    <HeroSection />
  </div>
</template>

<script>
import HeroSection from "~/components/HeroSection.vue";
export default {
  components: { HeroSection },
  name: "IndexPage",
};
</script>
