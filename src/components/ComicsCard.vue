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
  <a href="">
    <img :src="cardImage" alt="">
  </a>
    
    <h4>{{cardTitle}}</h4>
  </div>
 
</template>

<style scoped lang="scss">

.card{
  text-align:center;

  &:hover{
    transform: scale(1.1);
    transition: 1s;
        }
  


  img{
    max-width:100%;
    height: 150px;
  }

  h4{
    color:white;
    font-size: 0.7rem;
    text-transform: uppercase;

    &:hover{
          cursor:pointer;
        }
  }
}

</style>