<script>
export default {
  components: {},
  data() {
    return {
      menuFooter: [
        {
          title: "Characters",
        },
        {
          title: "Comics",
        },
        {
          title: "Movies",
        },
        {
          title: "Tv",
        },
        {
          title: "Games",
        },

        {
          title: "Videos",
        },

        {
          title: "News",
        },
      ],
      menuShop: [
        {
          title: "Shop DC ",
        },
        {
          title: "Shop DC Collectibles",
        },
      ],
      linkFooter: [
        {
          url: "footer-facebook.png",
        },
        {
          url: "footer-periscope.png",
        },
        {
          url: "footer-pinterest.png",
        },
        {
          url: "footer-twitter.png",
        },
        {
          url: "footer-youtube.png",
        },
      ],
    };
  },
  methods: {
    getImageUrl(imageName) {
      return new URL(`../assets/img/${imageName}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <footer>
    <div class="footer">
      <div class="content-footer-sx">
        <section>
          <h3>DC COMICS</h3>
          <ul>
            <li v-for="item in menuFooter">
              <a href="">{{ item.title }}</a>
            </li>
          </ul>
          <h3>SHOP</h3>
          <ul>
            <li v-for="item in menuShop">
              <a href="">{{ item.title }}</a>
            </li>
          </ul>
        </section>
        <section>
          <h3>DC</h3>
          <ul>
            <li v-for="item in menuFooter">
              <a href="">{{ item.title }}</a>
            </li>
          </ul>
        </section>
        <section>
          <h3>SITES</h3>
          <ul>
            <li v-for="item in menuFooter">
              <a href="">{{ item.title }}</a>
            </li>
          </ul>
        </section>
      </div>
      <div class="content-footer-dx">
        <section class="immag-footer"></section>
      </div>
    </div>
    <div class="cont-footer-down">
      <button type="">SING-UP NOW!</button>
      <div>
        <h3>FOOLLOW US</h3>
        <ul>
          <li v-for="image in linkFooter">
         
            <img :src="getImageUrl(image.url)" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/_mixin.scss" as *;
@use "../style/partials/_variables.scss" as *;

.footer {
  @include flex(row, space-between, center);
  background-image: url(../assets/img/footer-bg.jpg);
  width: 100%;
  position: relative;
  z-index: 1;
  margin: 0 auto;
  padding: 0 20px;

  .content-footer-sx {
    padding: 2rem 0;
    display: flex;
    flex-direction: row;
    width: 50%;

    h3 {
      color: white;
      margin: 0;
      @include flex(column, flex-start, flex-start);
      padding: 9px 5px;
    }

    ul {
      list-style-type: none;
      padding: 0;
      margin: 0 5px;
      @include flex(column, flex-start, flex-start);

      a {
        text-decoration: none;
        color: #ffffff40;
        font-size: 0.8rem;
      }
    }
  }
  .content-footer-dx {
    @include flex(column, space-around, flex-start);
    margin: 0 5px;
    width: 50%;

    .immag-footer {
      background-image: url(../assets/img/dc-logo.png);
      background-size: cover;
      position: absolute;
      top: 18px;
      right: 112px;
      width: 286px;
      height: 284px;
      z-index: 2;
      transform: rotate(31deg);
    }
  }
}
.cont-footer-down {
  background-color: $footer-color;
  height: 200px;
  @include flex(row, space-between, center);
  padding: 0 20px;

  button {
    background-color: $footer-color;
    border: 1px solid $active-color;
    color: white;
    font-weight: 900;
    padding: 10px;
    font-size: 1rem;
  }

  div{
    @include flex(row, space-between, center);

h3{
  margin-right: 30px;
  color:$active-color;
}


    ul{
      @include flex(row, space-between, center);
      list-style-type: none;
        gap: 1rem;
    }
  }
}
</style>
