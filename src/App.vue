<template>
  <section class="body">
    <Navigation />
    <Hero />
    <ContactForm />
  </section>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Hero from './components/Hero.vue';
import ContactForm from './components/ContactForm.vue';

export default {
  name: 'App',
  components: {
    Navigation,
    Hero,
    ContactForm
  }
}
</script>

