<template>
  <section class="hero md-layout-item">
    <picture>
      <img
        src="../assets/images/F-210_shadowed.png"
        alt="F-210 Drone Image"
        class="background-image"
      >
    </picture>
    <article class="body">
      <h1 class="jumbotron">F-210</h1>
      <h2 class="quote-body">"The Fastest Drone on the Planet"</h2>
      <p class="quote-source">&ndash;The Wirecutter</p>
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