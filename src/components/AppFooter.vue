<script>



export default {
    components:{
       
    },
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
    };
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
            <li v-for='item in menuFooter'><a href="" >{{item.title}}</a></li>
        </ul>
        <h3>SHOP</h3>
        <ul>
            <li v-for='item in menuShop'><a href="" >{{item.title}}</a></li>
        </ul>
      </section>
      <section>
        <h3>DC</h3>
        <ul>
            <li v-for='item in menuFooter'><a href="" >{{item.title}}</a></li>
        </ul>
        
      </section>
      <section>
        <h3>SITES</h3>
        <ul>
            <li v-for='item in menuFooter'><a href="" >{{item.title}}</a></li>
        </ul>
      </section>
    </div>
    <div class="content-footer-dx">
        <section class="immag-footer">
       <img src="../assets/img/dc-logo.png" alt=""> 
      </section>
    </div>
      
    </div>
  </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/_mixin.scss" as *;

.footer{

    @include flex(row, flex-start, flex-start);
    background-image: url(../assets/img/footer-bg.jpg);


.content-footer-sx {
  padding: 5rem 0;
  display: flex;
  flex-direction: row;
  

  h3{
    color: white;
    margin: 0;
    @include flex(column, flex-start, flex-start);
    padding: 0 5px;
   
  }

  ul{
    list-style-type: none;
    padding: 0;
    margin:0 5px;
    @include flex(column, flex-start, flex-start);

    a{
        text-decoration: none;
        color: #ffffff40;
        font-size: 0.8rem;
       
    }
}

section{
    @include flex(column, flex-start, flex-start);
   margin:0 5px;
  
  .immag-footer{
    flex-direction: flex-and;
   }

}

}
}
</style>
