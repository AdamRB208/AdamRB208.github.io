<script setup>

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
            <i class="mdi mdi-github fs-1"></i>
          </a>
        </button>
        <button class="btn" type="button" title="To My LinkedIn">
          <a href="https://www.linkedin.com/in/adam-borup-0a0911265?trk=people-guest_people_search-card"
            target="_blank">
            <i class="mdi mdi-linkedin fs-1"></i>
          </a>
        </button>
      </div>
      <div class="d-flex justify-content-center">
        <form target="_blank" action="">
          <div class="mb-3">
            <input type="email" class="form-control" id="exampleFormControlInput1"
              placeholder="To: Adamrborup@gmail.com">
          </div>
          <div class="mb-3">
            <input type="title" class="form-control" id="exampleFormControlInput1" placeholder="Title:">
          </div>
          <div class="mb-3">
            <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"
              placeholder="Email Body:"></textarea>
          </div>
          <div class="mb-1">
            <button class="btn btn-rounded btn-primary send-btn text-white" title="Send Message">Send Message <i
                class="mdi mdi-email-fast-outline ms-1 fs-5"></i></button>
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
  width: 80%;
  text-align: center;
}
</style>