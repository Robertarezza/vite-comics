<script >


export default {
  data() {
    return {
        menuHeader: [
            {
                title: "Characters",
                isActive: false
            },
            {
                title: "Comics",
                isActive: true
            },
            {
                title: "Movies",
                isActive: false
            },
            {
                title: "Tv",
                isActive: false
            },
            {
                title: "Games",
                isActive: false
            },
            {
                title: "Collectibles",
                isActive: false
            },
            {
                title: "VIDEOS",
                isActive: false
            },
            {
                title: "FANS",
                isActive: false
            },
            {
                title: "NEWS",
                isActive: false
            },
            {
                title: "SHOP",
                isActive: false
            },
        ]
    };
  },
};
</script>


<template>
<header>
<div class="header-logo">
    <img src="../assets/img/dc-logo.png" alt="">
</div>
   
    <ul class="navigation">
        
        <li v-for='item in menuHeader'><a href="" :class="{active: item.isActive}">{{item.title}}</a></li>
       
    </ul>
</header>
</template>

<style scoped lang="scss">
@use "../style/partials/_mixin.scss" as *;
@use "../style/partials/_variables.scss" as *;



header{
    @include flex(row, space-around, center);
    padding: 8px 0;
    margin-bottom:0;

    ul{
        @include flex(row, center, flex-end);
        list-style-type: none;
        gap: 1rem;

        a{
            text-decoration: none;
            color: $text-color;
            // font-size: 1.5rem;
            text-transform: uppercase;
            padding-bottom:50px;

            &.active {
                color: $active-color;
                border-bottom:4px solid $active-color;
             
            }
        }
    }
}

</style>