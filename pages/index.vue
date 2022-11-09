<template>
  <div>
    <HeroSection />
    <AboutUs />
    <Service />
    <Collection />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
    head() {
    return {
      title: "Renty",
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
