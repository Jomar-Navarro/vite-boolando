<script>
import { footerMenues } from '../assets/data/menues'
  export default {
    computed: {
      socialMenu(){
        return footerMenues.social
      }
    }
  }
</script>


<template>
  <footer>
    <div class="container d-flex">
      <div>
        <h4>Boolando s.r.l</h4>
        <nav>
          <ul class="d-flex">
            <li><a href="#">Infomazioni legali</a></li>
            <li><a href="#">Normativa sulla privacy</a></li>
            <li><a href="#">Diritto di recesso</a></li>
          </ul>
        </nav>
      </div>

      <div class="social">
        <h4>Trovaci anche su</h4>
        <ul>
          <li><a v-for="(item, index) in socialMenu" :key="`s-${index}`" :href="`${item.link}`" v-html="`${item.title}`"></a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

  footer{
    display: flex;
    align-items: center;
    background-color: $bf-footer-color;
    height: 100px;
      .container{
        justify-content: space-between;
        color: white;
        ul li{
          padding: 0;
          line-height: 40px;
          padding-right: 10px;
          a{
            text-decoration: none;
            color: white;
          }
        }
      }
  }

  .social{
    ul{
      li{
        a{
          color:white;
          padding: 0 5px;
          i{
            font-size: large;
            line-height: 40px;
          }
        }
      }
    }
    

    
  }

</style>