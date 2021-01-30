<template>
  <section class="modal-background">
    <article class="modal-body">
      <form @submit="validateForm" novalidate="true">
        <fieldset>
          <label for="name">Full Name</label>
          <input
            name="name"
            type="text"
            placeholder="Enter your full name"
            v-model.lazy="name"
            @change="isValid"
          />
          <span class="error" v-if="errors.name">Full Name is required</span>
        </fieldset>

        <fieldset>
          <label for="email">Email</label>
          <input
            name="email"
            type="email"
            placeholder="Enter your email"
            v-model.lazy="email"
            @change="isValid"
          />
          <span class="error" v-if="errors.email">Email is required and must contain a valid email address</span>
        </fieldset>

        <fieldset>
          <label for="message">Message</label>
          <textarea
            name="message"
            placeholder="What are your plans?"
            v-model.lazy="message"
            @change="isValid"
          ></textarea>
          <span class="error" v-if="errors.message">Message is required</span>
        </fieldset>

        <fieldset>
          <button type="submit" class="primary" :disabled="invalid">Send Message &#8594;</button>
        </fieldset>
      </form>
    </article>
  </section>
</template>

<script>
export default {
  name    : 'ContactForm',
  props   : {},
  methods : {
    // Check for a valid email address
    validEmail: function (email) {
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    },
    // Upon any change to the form, check if all the inputs are valid
    // and use that to determine whether or not the submit button is enabled
    isValid() {
      var isNameValid = this.name.length > 0;
      var isEmailValid = this.email.length > 0;
      var isMessageValid = this.message.length > 0;

      if (isNameValid && isEmailValid && isMessageValid) {
        this.invalid = false;
      } else {
        this.invalid = true;
      }
    },
    // Upon form submit, check for errors and, if present, switch
    // specific error statuses to show relevant errors on form
    validateForm(e) {
      if (this.name.length <= 0) {
        this.errors.name = true;
        this.invalid = true;
      }

      if ((this.email.length <= 0) || (!this.validEmail(this.email))) {
        this.errors.email = true;
        this.invalid = true;
      }

      if (this.message.length <= 0) {
        this.errors.message = true;
        this.invalid = true;
      }

      // If there are errors, do not submit the form
      if (this.invalid) {
        e.preventDefault();
      }

    }
  },
  data() {
    return {
      name    : '',
      email   : '',
      message : '',
      invalid : true,
      errors  : {
        name    : false,
        email   : false,
        message : false
      }
    }
  }
}
</script>