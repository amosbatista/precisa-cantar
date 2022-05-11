<template>
  <nav class="container">
    <div class="container-center">
      <nuxt-content :document="navLinks" />
    </div>
  </nav>
</template>

<script>
export default {
  name: 'PageMenu',
  props: ['navLinks']
}
</script>

<style>
  nav {
    background-color: #41237b;
  }
  nav ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
    list-style: none;
    padding-left: 0px;
  }
  .home nav li {
    margin: 0 0 0 10px;
  }
  nav li {
    margin: 0 0 0 10px;
  }
  nav a {
    color: #efe0b3;
    font-size: 75%;
    display: inline-flex;
    margin: 0;
  }
</style>
