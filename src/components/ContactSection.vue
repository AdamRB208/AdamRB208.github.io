<script setup>
import { ref } from 'vue';


const formData = ref({
  users_email: '',
  subject: '',
  message: ''
})


</script>


<template>
  <div class="col-12 d-flex justify-content-center mt-5">
    <div class="d-block justify-content-center">
      <div>
        <p class="d-flex justify-content-center fs-2 mb-5">Looking to get in contact?</p>
        <p class="mb-4" style="margin: 1.5em;">You can contact me via email below or any of my socials listed below. I
          look forward to
          hearing from you.
        </p>
      </div>
      <div class="d-flex justify-content-center mb-4">
        <button class="btn" type="button" title="To My Github">
          <a href="https://github.com/AdamRB208" target="_blank">
            <i class="mdi mdi-github fs-1 text-glow"></i>
          </a>
        </button>
        <button class="btn" type="button" title="To My LinkedIn">
          <a href="https://www.linkedin.com/in/adamrborup" target="_blank">
            <i class="mdi mdi-linkedin fs-1 text-glow"></i>
          </a>
        </button>
      </div>
      <div class="d-flex justify-content-center">
        <form target="_blank" action="">
          <div class="mb-3">
            <input type="email" name="users_email" placeholder="Your Email Address" required>
          </div>
          <div class="mb-3">
            <input type="text" name="subject" placeholder="Subject" required>
          </div>
          <div class="mb-3">
            <textarea name="message" rows="3" placeholder="Your Message"></textarea>
          </div>
          <div class="mb-1">
            <button class="btn btn-rounded btn-glow send-btn text-dark mb-4" type="submit" title="Send Message">Send
              Message <i class="mdi mdi-email-fast-outline ms-1 fs-5"></i></button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
a {
  text-decoration: none;
  color: inherit
}

form {
  width: 80%;
}

.send-btn {
  width: 100%;
}
input {
  width: 100%;
}

textarea {
  width: 100%;
}
i {
  text-shadow: 1px 1px 10px #b6b0b0;
}
</style>