<script>
export default {
  props: {
    title: String,
  },
};
</script>

<template>

    <button type="">
      <a @click.prevent href="">
        {{ title }}
      </a>
    </button>
 
</template>

<style lang="scss" scoped>

@use "../style/partials/_variables.scss" as *;


  button {
    background-color: $active-color;
    font-weight: 900;
    padding: 10px;
    font-size: 1rem;


  &:hover {
    transform: scale(1.1);
    transition: 1s;
  }

  a {
    color: white;
    text-decoration: none;
    font-weight: 800;
  }
}

</style>
