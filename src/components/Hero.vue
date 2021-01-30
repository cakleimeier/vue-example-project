<template>
  <section class="hero md-layout-item">
    <picture>
      <img src="../assets/images/F-210_shadowed.png" alt="F-210 Drone Image" class="background-image">
    </picture>
    <article class="body">
      <h1 class="md-display-4">F-210</h1>
      <h2 class="md-display-1">"The Fastest Drone on the Planet"</h2>
      <p class="md-subheading">The Wirecutter</p>
    </article>
  </section>
</template>

<script>
export default {
  name: 'Hero',
  props: {},
  data() {
    return {
      publicPath: process.env.BASE_URL
    }
  }
}
</script>