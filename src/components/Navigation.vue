<template>
  <section class="navigation md-layout-item md-size-100 md-layout md-gutter">
    <!-- 175px -->
    <div class="md-layout-item md-size-25 md-layout md-layout-gutter">
      <!-- Left nav -->
      <div class="md-layout-item md-size-50">
        <a href="#" class="nav-item">Store</a>
      </div>
      <div class="md-layout-item md-size-50">
        <a href="#" class="nav-item">Tutorials</a>
      </div>
    </div>

    <!-- Logo -->
    <div class="md-layout-item md-size-50">
      <img
        src="../assets/logo.png"
        alt="Byrd MD logo"
        class="nav-logo"
      >
    </div>

    <!-- Center nav -->
    <div class="md-layout-item md-size-25 md-layout md-layout-gutter">
      <div class="md-layout-item md-size-50">
        <a href="#" class="nav-item">Blog</a>
      </div>
      <div class="md-layout-item md-size-50">
        <a href="#contact" class="nav-item">Contact</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Navigation',
  props: {}
}
</script>