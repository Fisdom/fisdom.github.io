<template>
  <main  class="about-container mtl-s mtf-m">
    <div class="row center-align pbm-s">
        <div class="h2"><span class="border-thick">Contact Me</span></div>
      </div>
    <div class="row">
      <div class="col s12 m10 offset-m1">
        <form method="POST" action="https://tierion.com/form/submit">
          <input name="_key" type="hidden" value="yrQNjwDHIUeYDT8VDYPM6A">
          <div class="input-field">
            <input type="text" id="name" name="name" v-model="name">
            <label for="name">Name</label>  
          </div>
          <div class="input-field">
            <input type="email" id="email" name="email" v-model="email">
            <label for="email">E-mail</label>
          </div>
          <div class="input-field">
            <input type="text" id="message" name="message" v-model="message">
            <label for="message">Message</label>
          </div>
          <div class="center-align"><button class="btn green" type="submit" v-bind:disabled="!isValid">Submit</button></div>
        </form>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'contact',
  data: function () {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  computed: {
    isValid: function () {
      return this.name !== '' && this.email !== ''
    }
  }
}
</script>
