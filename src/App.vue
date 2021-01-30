<template>
  <section class="body">
    <Navigation />
    <Carousel />
    <ContactForm />
  </section>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Carousel from './components/Carousel.vue';
import ContactForm from './components/ContactForm.vue';

export default {
  name: 'App',
  components: {
    Navigation,
    Carousel,
    ContactForm
  }
}
</script>

