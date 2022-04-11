<template>
  <section class="blog-posts">
    <svg
      class="fusion-big-triangle-candy mb-4 testing-rotate"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: #ffffff; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
    <div class="row centralize-paragraph">
      <div class="col-6 text-paragraph">
        <h5>TALES FROM THE BARBER SHOP</h5>
        <h3>Recent Blog Posts</h3>
      </div>
      <div class="col-12">
        <ul class="posts-list">
          <li v-for="(post, index) in posts" :key="index">
            <div>
              <img
                :src="require(`@/assets/images/Blog-Posts/${post.image}`)"
                class="img-fluid"
                :alt="`icon of ${post.title}`"
              />
              <div class="text-body">
                <h3 class="">{{ post.title }}</h3>
                <p class="">
                  {{ post.description }}
                </p>
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div class="col-6">
        <button class="my-btn-style">read more from our blog</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BlogPosts",
  data: function () {
    return {
      posts: [
        {
          image: "avadabarbers-second-blog-700x441.jpg",
          title: "Avada Barbers Now Open",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
        {
          image: "avadabarbers-choosing-blog-700x441.jpg",
          title: "Choosing The Right Barber",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
        {
          image: "avadabarbers-ourservice-blog-700x441.jpg",
          title: "Quick Service Guide",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "/src/assets/scss/style.scss";
section.blog-posts {
  background-color: $Ebb;
  .centralize-paragraph {
    width: 50vw;
    margin: 0 auto;
    padding: 3rem 0;
    .text-paragraph {
      width: 100%;
    }
    ul.posts-list {
      display: flex;
      justify-content: space-evenly;
      li {
        list-style-type: none;
        img {
          padding: 1rem;
          margin-bottom: 1rem;
        }
        .text-body {
          padding: 1rem 3rem;
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
  .testing-rotate {
    rotate: (180deg);
  }
}
</style>
