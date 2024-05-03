<script >


export default {
  props: {
        cardImage: String,
        cardTitle: String,
      },
  data() {
    return {
      
    
    };
  },
};
</script>


<template>
  <div class="card">
    <img :src="cardImage" alt="">
    <h4>{{cardTitle}}</h4>
  </div>
 
</template>

<style scoped lang="scss">

.card{
  text-align:center;


  img{
    max-width:100%;
    height: 150px;
  }

  h4{
    color:white;
    font-size: 0.7rem;
    text-transform: uppercase;
  }
}

</style>