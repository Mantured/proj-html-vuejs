<template>
  <!-- <section class="container-fluid"> -->
  <section class="container-fluid">
    <div class="products container">
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
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Products",
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
