<template>
  <!-- valutare il caso di creare due component diversi services product-->
  <main>
    <Services />
    <!-- <div class="services container">
      <div class="row centralize-paragraph">
        <div class="col-6 text-paragraph">
          <h5>mens grooming</h5>
          <h3>Services</h3>
        </div>
        <div class="col-12">
          <ul class="services-list">
            <li v-for="(service, index) in servicesLink" :key="index">
              <div>
                <img
                  :src="require(`@/assets/images/Services/${service.image}`)"
                  class=""
                  :alt="`icon of ${service.title}`"
                />
                <div class="text-body">
                  <h3 class="">{{ service.title }}</h3>
                  <p class="">
                    {{ service.description }}
                  </p>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="col-6">
          <button class="btn my-btn-style">read about our services</button>
        </div>
      </div>
    </div> -->
    <svg
      class="fusion-big-triangle-candy mt-5"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: $coldGrey; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
    <Products />
  </main>
</template>

<script>
import Services from "./Services.vue";
import Products from "./Products.vue";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Main",
  components: {
    Services,
    Products,
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
