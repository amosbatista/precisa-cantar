<template>
  <div>
    <header>
      <img class="banner" src="/header/precisa-cantar-banner.jpg">
      <!--<div class="bg">
        <div class="bg-image" />
        <div class="bg-gradient" />
        <div class="bg-title">
          <div class="container">
            <div class="container-center">
              <a class="header-title" href="\">
                <i>"Precisa cantar, senhora?"</i>
              </a>
            </div>
          </div>
        </div>
      </div>-->
    </header>
    <page-menu :nav-links="navLinks" />
  </div>
</template>

<script>
import pageMenu from './pageMenu/index.vue'
export default {
  components: { pageMenu },
  props: ['navLinks']
}
</script>

<style>
  header {
    height: 300px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    justify-content: center;
  }
  .banner {
    width: 55%;
  }
  @media (max-width: 700px) {
    header {
      height: 200px;
    }
    .banner {
      width: 80%;
    }
  }
  @media (max-width: 300px) {
    header {
      height: 150px;
    }
    .banner {
      width: 100%;
    }
  }
  .bg {
    height: 200px;
    width: 100%;
    display: flex;
    align-items: flex-end;
    justify-content: flex-start;
    border-bottom: 3px solid #91946c;
    position: relative;
  }
  .bg-gradient {
    width: 100%;
    height: 100%;
    position: absolute;
    background: linear-gradient(90deg, rgba(25,7,73,1) 34%, rgba(0,212,255,0) 100%);
  }
  .bg-image {
    position: absolute;
    width: 100%;
    height: 100%;
    background-image: url('/header/bg1.jpg');
    background-position: center;
    background-size: cover;
  }
  .bg-title {
    position: absolute;
    width: 100%;
    bottom: 30px;
  }
  .header-title {
    font-size: 165%;
    margin-bottom: 15px;
    font-weight: 700;
  }
  .header-title,
  .header-title a,
  .header-title a:visited {
    text-decoration: none;
    color: #dbcc22;
  }
</style>
