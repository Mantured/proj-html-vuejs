<template>
  <main>
    <Services />
    <svg
      class="fusion-big-triangle-candy mt-5"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: #121315; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
    <Products />
    <Reviews />
    <BlogPosts />
  </main>
</template>

<script>
import Services from "./Main/Services.vue";
import Products from "./Main/Products.vue";
import Reviews from "./Main/Reviews.vue";
import BlogPosts from "./Main/BlogPosts.vue";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Main",
  components: {
    Services,
    Products,
    Reviews,
    BlogPosts,
  },
  data: function () {
    return {};
  },
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";
</style>
