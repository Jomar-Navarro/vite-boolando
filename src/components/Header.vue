<script>
  import { headerMenues } from '../assets/data/menues'
  export default {

    data(){
      return{
      }
    },
    computed: {
      mainMenu(){
        return headerMenues.menu;
      },

      socialMenu(){
        return headerMenues.social;
      }
    },
  }
</script>


<template>
  <header>
    <div class="container d-flex ">
      <nav class="menu d-flex ">
        <ul class="d-flex">
          <li v-for="(item, index) in mainMenu" :key="`m-${index}`"><a :href="item.link">{{ item.title }}</a>
          </li>
        </ul>
      </nav>

      <div class="logo d-flex ">
        <img src="/src/assets/img/boolean-logo.png" alt="logo">
      </div>

      <div class="icons">
        <ul>
          <li v-for="(item, index) in socialMenu" :key="`s-${index}`" v-html="`${item.title}`"></li>
        </ul>
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

  header{
    position: sticky;
    top: 0;
    z-index: 100;
    justify-content: center;
    background-color: $bg-header-color;
    height: 80px;
    box-shadow: 0px 1px 4px 0px;
    .container{
      justify-content: space-between;
      align-items: center;
      height: 100%; 
      ul li{
        color: white;
        padding: 5px;
        font-size: 1rem;
        font-weight: 800;
      }
    }
  }

  .container{
    .logo{
      img{
        height: 40px;
      }
    } 
  }

  .icons{
    ul{
      display: flex;
      li{
        i {
            padding: 0px 5px;
            color: white;
          }
      }
    }
  } 
  
</style>