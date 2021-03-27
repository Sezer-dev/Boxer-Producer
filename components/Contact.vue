<template>
  <div id="contact" class="container-fluid my-md-5 my-3 py-md-5 py-3">
    <div class="row d-flex justify-content-center">
      <div class="col-12 d-flex justify-content-center">
        <div class="contact-header">
          <p class="mb-1 mb-md-3">Contact Us</p>
          <span class="line"></span>
        </div>
      </div>
    </div>
    <div class="row d-flex justify-content-center my-5">
      <div
        class="col-12 d-flex flex-md-row flex-column justify-content-md-between justify-content-center align-items-center"
      >
        <div class="col-md-7 col-10">
          <div class="d-flex justify-content-between">
            <div class="text-container">
              <p class="contact-text">
                <span class="contact-icon">T</span>+90 212 514 80 80
              </p>
            </div>
            <div class="text-container">
              <p class="contact-text">
                <span class="contact-icon">W</span>+90 538 297 63 73
              </p>
            </div>
          </div>
          <div class="d-flex justify-content-between pb-md-5">
            <div class="text-container">
              <p class="contact-text">
                <span class="contact-icon">F</span>+90 212 210 06 06
              </p>
            </div>
            <div class="text-container">
              <p class="contact-text">
                <span class="contact-icon">E</span>info@kucukaslantekstil.com
              </p>
            </div>
          </div>
          <div
            class="d-flex flex-column align-items-center align-items-md-start pt-md-5"
          >
            <p class="contact-text">
              <span class="contact-icon d-inline-block">A</span>Seyrantepe
              Yıldız St. Number:5
            </p>
            <p class="contact-text">Kagithane / Istanbul, Turkey</p>
          </div>
        </div>
        <div class="col-md-5 col-12">
          <b-form>
            <b-form-group
              id="input-group-name"
              label="Name & Surname"
              label-for="input-name-surname"
              @submit="onSubmit"
            >
              <b-form-input
                id="input-name-surname"
                v-model="form.fullName"
                type="text"
                required
                class="form-input"
              ></b-form-input>
            </b-form-group>
            <b-form-group
              id="input-group-email"
              label="E-mail"
              label-for="input-email"
            >
              <b-form-input
                id="input-email"
                v-model="form.email"
                type="email"
                required
                class="form-input"
              ></b-form-input>
            </b-form-group>
            <b-form-group
              id="input-textarea"
              label="Message"
              label-for="input-message"
            >
              <b-form-textarea
                id="input-textarea"
                v-model="form.message"
                required
                rows="4"
                class="form-input"
              ></b-form-textarea>
            </b-form-group>
            <b-button type="submit" class="input-submit-button mr-3"
              >Send</b-button
            >
          </b-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        fullName: "",
        email: "",
        message: "",
      },
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
    },
  },
}
</script>

<style scoped>
.contact-header {
  font-size: 36px;
}
.line {
  border-bottom: 4px solid #d81a04;
  display: block;
}
.text-container {
  width: 240px;
}
.contact-text {
  font-size: 18px;
}
.contact-icon {
  color: #d81a04;
  font-size: 18px;
  width: 17px;
  display: inline-block;
}
.form-input {
  background: #f9f9f9;
  border-radius: 12px;
}
.input-submit-button {
  position: absolute;
  right: 0;
  height: 50px;
  width: 145px;
  font-size: 18px;
  background: #000000;
  border-radius: 25px;
}
.form-group,
.form-input {
  font-size: 24px;
}
@media screen and (max-width: 768px) {
  .input-submit-button {
    font-size: 9px;
    width: 67px;
    height: 28px;
  }
  .contact-icon,
  .contact-text {
    font-size: 14px;
  }
  .form-group,
  .form-input {
    font-size: 14px;
    width: 100%;
  }
  .contact-header {
    font-size: 18px;
  }
  .text-container {
    width: 129px;
  }
}
</style>
