<template>
  <nav class="container">
    <div class="container-center">
      <ul>
        <li v-for="link, key in navLinks" :key="key">
          {{ link }}
        </li>
      </ul>
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

</style>
