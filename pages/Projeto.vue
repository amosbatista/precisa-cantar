<template>
  <div id="page">
    <page-header />
    <div class="container">
      <div class="container-center page-content">
        <div class="logo-sobre">
          <img src="logo-unirio.png">
        </div>
        <nuxt-content :document="page" />
      </div>
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('pages/projeto').fetch()

    return {
      page
    }
  }
}
</script>

<style>
  .logo-sobre {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 50px 0 25px;
  }
  .logo-sobre img {
    max-width: 500px;
  }
</style>
