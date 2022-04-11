<template>
  <!-- <section class="container-fluid"> -->
  <section class="services">
    <div class="centralize-container">
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
          <button class="my-btn-style">read about our services</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Services",
  data: function () {
    return {
      servicesLink: [
        {
          image: "avadabarbers-trimcut-icon-before.png",
          title: "trim & cut",
          description:
            "Avada Barbers are experts in the lickety split and hair cut. Quick but careful and ridiculously good looking",
        },
        {
          image: "avadabarbers-washndry-icon.png",
          title: "wash & dry",
          description:
            "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion",
        },
        {
          image: "avadabarbers-beardtrim-icon.png",
          title: "beard tidy",
          description:
            "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers",
        },
      ],
    };
  },
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "/src/assets/scss/style.scss";
section.services {
  .centralize-paragraph {
    height: 90vh;
    ul.services-list {
      display: flex;
      justify-content: space-evenly;
      li {
        list-style-type: none;
        img {
          padding: 1rem;
          margin-bottom: 1rem;
          scale: 0.45;
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
