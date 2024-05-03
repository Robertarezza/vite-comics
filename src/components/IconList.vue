<script>
export default {
  data() {
    return {
      images: [
        {
          name: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
        },
        {
          name: "buy-comics-merchandise.png",
          title: "DC MERCHANDISE",
        },
        {
          name: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
        },
        {
          name: "buy-dc-power-visa.svg",
          title: "COMIC SHOP LOCATOR",
        },
        {
          name: "buy-comics-subscriptions.png",
          title: "DC POWER VISA",
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
  <section>
    <ul>
      <li v-for="image in images">
        <img :src="getImageUrl(image.name)" alt="" />
        <h4>{{ image.title }}</h4>
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
@use "../style/partials/_variables.scss" as *;
@use "../style/partials/_mixin.scss" as *;

section {
  background-color: $active-color;
  color: white;
  padding:3rem 0;

  ul {
    list-style-type: none;
    @include flex(row, space-evenly, center);

    li {
      @include flex(center, center, center);
      gap: 1rem;
      img {
        height: 50px;
      }

      h4 {
        font-weight: 200;
        font-size: 0.8rem;
      }
    }
  }
}
</style>
