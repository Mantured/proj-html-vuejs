<template>
  <section class="header-wrapper" id="home">
    <div class="container-fluid position-fixed my-background">
      <div class="header-top">
        <div class="row">
          <div class="col-3">
            <img
              src="../assets/images/Logo/avadabarbers-logo-x2-200x70.png"
              alt="logo avada barbers"
            />
          </div>
          <div class="col align-item-center d-flex justify-content-end">
            <div>
              <i class="fas fa-shopping-cart me-3"></i>
            </div>
            <div class="">
              <button
                class="btn dropdown-toggle position-relative my-index"
                type="button"
                id="dropdownMenuButton1"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                <i class="fas fa-bars"></i>
              </button>
              <ul id="my-dropdown" class="dropdown-menu">
                <li v-for="(link, index) in linksNav" :key="index">
                  <a
                    id="my-drop-item"
                    class="dropdown-item"
                    :href="link.link"
                    >{{ link.name }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="header-bottom">
      <div class="row h-100">
        <div
          class="col d-flex flex-column justify-content-center align-items-start"
        >
          <h1>Barber Shop</h1>
          <!-- div interim -->
          <div class="separator"></div>
          <p>The Pinnacle of Male Grooming</p>
          <button class="my-btn-style">learn more</button>
        </div>
        <div class="col-6 h-100">
          <img
            class="img-fluid h-100"
            src="../assets/images/Header-Jumbo/avadabarbers_hero_focalmirror-800x1100.png"
            alt="barber cutting hair"
          />
        </div>
      </div>
      <i class="fab fa-opencart"></i>
      <i class="fab fa-wpressr"></i>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  data: function () {
    return {
      linksNav: [
        {
          link: "#home",
          name: "Home",
        },
        {
          link: "#services-link",
          name: "Services",
        },
        {
          link: "#shop-link",
          name: "Shop",
        },
        {
          link: "#",
          name: "Our Team",
        },
        {
          link: "#blog-link",
          name: "Blog",
        },
        {
          link: "#",
          name: "Contact Us",
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
section.header-wrapper {
  height: 100vh;
  background-size: cover;
  background-position: center;
  background-image: url(../assets/images/Header-Jumbo/avadabarbers-homepage-hero-bg.jpg);
  div.header-top,
  div.header-bottom {
    width: 70vw;
    margin: 0 auto;
  }
  div.header-top {
    /* width: 70vw;
    margin: 0 auto; */
    /* position: fixed;
    top: 0;
    left: 50%; */
    line-height: 120px;
    position: relative;
    /* transform: translateX(-50%); */
    i {
      color: #ffffff;
      font-size: 1.5rem;
    }
  }
  div.header-bottom {
    /* width: 70vw;
    margin: 0 auto; */
    height: 85%;
    line-height: 85px;
    position: relative;
    top: 196px;
    h1 {
      font-size: 5.5rem;
    }
    div.separator {
      width: 16rem;
      border: 0.4px solid $Driftwood;
    }
    p {
      color: $Emperor;
      font-size: 1.5rem;
    }
    i {
      right: 5px;
      width: 60px;
      /*       z-index: 3; */
      padding: 0.5rem;
      font-size: 2rem;
      position: fixed;
      text-align: center;
      color: $KashmirBlue;
      border-radius: 0.3rem;
      background-color: white;
      &.fab.fa-opencart {
        top: 180px;
      }
      &.fab.fa-wpressr {
        top: 235px;
      }
    }
  }
}

ul#my-dropdown {
  /* inset: unset !important; */
  margin: 0px;
  transform: translate3d(-384.244px, 0px, 0px) !important;
  height: 100vh;
  width: 100vw;
  background: rgba(0, 0, 0, 0.85);
  padding-top: 12rem;
}
#dropdownMenuButton1 {
  color: transparent;
}

#my-drop-item {
  color: white;
  text-align: center;

  font-size: 3rem;
  &:hover {
    background-color: rgba(251, 141, 5, 0.5) !important;
  }
}

.fas.fa-shopping-cart {
  margin-top: 49px;
}
.my-background {
  background: rgba(0, 0, 0, 0.5);
  z-index: 1;
}
</style>
