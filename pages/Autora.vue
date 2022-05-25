<template>
  <div id="page">
    <page-header />
    <div class="container">
      <div class="container-center page-content autora">
        <div class="foto-sobre">
          <img src="foto-debora-export.jpg">
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
    const page = await $content('pages/autora').fetch()

    return {
      page
    }
  }
}
</script>

<style>
  .foto-sobre {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 50px 0 25px;
  }
  .foto-sobre img {
    max-width: 500px;
  }
</style>
