<template>
  <!-- <section class="container-fluid"> -->
  <section class="container-fluid">
    <div class="products container">
      <div class="row centralize-paragraph">
        <div class="col text-paragraph">
          <h5>we have you covered</h5>
          <h3>avada grooming products</h3>
        </div>
        <div class="col-12">
          <ul class="products-list">
            <li v-for="(product, index) in productsLink" :key="index">
              <div>
                <img
                  :src="require(`@/assets/images/Products/${product.image}`)"
                  class="img-fluid"
                  :alt="`icon of ${product.title}`"
                />
                <div class="text-body">
                  <h3 class="">{{ product.title }}</h3>
                  <p class="">
                    {{ product.price }}
                  </p>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="col-6">
          <button class="btn my-btn-style"></button>
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
    return {
      productsLink: [
        {
          image: "brush_dark.png",
          title: "brush",
          price: "15.00",
        },
        {
          image: "scissors.png",
          title: "scissor",
          price: "85.00",
        },
        {
          image: "hot_oil_dark.png",
          title: "hot oil",
          price: "15.00",
        },
        {
          image: "straight_razor_dark.png",
          title: "straight razor",
          price: "30.00",
        },
      ],
    };
  },
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";
div.products {
  .centralize-paragraph {
    height: 90vh;
    ul.products-list {
      display: flex;
      justify-content: space-evenly;
      li {
        list-style-type: none;
        img {
          padding: 1rem;
          margin-bottom: 1rem;
        }
        .text-body {
          width: 250px;
          h3 {
            color: $Driftwood;
            text-transform: capitalize;
            margin-bottom: 2rem;
          }
          p {
            color: $SilverChalice;
          }
        }
      }
    }
  }
}
</style>
