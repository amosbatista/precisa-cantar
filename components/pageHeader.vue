<template>
  <header>
    <div class="bg">
      <div class="bg-image">
      </div>
      <div class="bg-gradient">
      </div>
      <span class="header-title">
        <a href="\">
          Precisa cantar?
        </a>
      </span>
    </div>
  </header>
</template>

<script>

export default {
}
</script>

<style>
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
  .header-title {
    position: absolute;
    margin-left: 30px;
    margin-bottom: 15px;
    font-weight: 700;
  }
  header a {
    text-decoration: none;
  }
</style>
