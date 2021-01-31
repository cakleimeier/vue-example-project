<template>
  <section class="body md-layout">
    <Navigation @open="open"/>
    <Hero />
    <ContactForm @submitForm="submitForm" :open="openModal"/>
    <div class="success-message" v-if="formSubmitted">
      <h6>Your form has been submitted!</h6>
      <button class="close-button" @click="closeSuccessMessage">OK</button>
    </div>
  </section>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Hero from './components/Hero.vue'
import ContactForm from './components/ContactForm.vue'

export default {
  name: 'App',
  components: {
    Navigation,
    Hero,
    ContactForm
  },
  methods : {
    open() {
      this.openModal = true;
    },
    submitForm() {
      this.formSubmitted = true;
    },
    closeSuccessMessage() {
      this.formSubmitted = false;
    }
  },
  data() {
    return {
      openModal: false,
      formSubmitted : false
    }
  }
}
</script>

