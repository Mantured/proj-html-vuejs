<template>
  <section class="best-product-reviews">
    <div class="months-product container">
      <div
        class="row product"
        v-for="(product, index) in bestProduct"
        :key="index"
        :class="product.statusReview === true ? 'active' : ''"
      >
        <div class="col-4 product-image">
          <img
            :src="require(`@/assets/images/Products/${product.image}`)"
            class="img-fluid"
            :alt="`icon of ${product.title}`"
          />
        </div>
        <div class="col-8 text-paragraph product-description">
          <h5>this months featured product</h5>
          <h3>{{ product.title }}</h3>
          <p>{{ product.description }}</p>
          <button class="btn my-btn-style">buy now</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Reviews",
  data: function () {
    return {
      bestProduct: [
        {
          image: "shaving_butter.png",
          title: "shaving butter",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          statusReview: true,
        },
        {
          image: "brush_dark.png",
          title: "brush",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          statusReview: false,
        },
        {
          image: "scissors.png",
          title: "scissor",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          statusReview: false,
        },
        {
          image: "hot_oil_dark.png",
          title: "hot oil",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          statusReview: false,
        },
        {
          image: "straight_razor_dark.png",
          title: "straight razor",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          statusReview: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
.product {
  width: 50vw;
  height: 40vh;
  bottom: 40px;
  display: none;
  margin: 0 auto;
  position: relative;
  align-items: center;
  border-top: 3px solid $Goldenrod;
  &.active {
    display: flex;
  }
  .product-image {
    height: 100%;
    background-image: url(../assets/images/avadabarbers-cta-background.jpg);
    background-size: cover;
    background-position: center;
    img {
      height: 100%;
      object-fit: contain;
    }
  }
  .product-description {
    height: 100%;
    padding: 2rem 4.5rem;
    background-color: $ColdGrey;
    p {
      color: $Emperor;
    }
  }
}
</style>
