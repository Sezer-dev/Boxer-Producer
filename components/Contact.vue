<template>
  <div id="contact" class="container-fluid my-md-5 my-3 py-md-5 py-3">
    <div class="row d-flex justify-content-center">
      <div class="col-11 d-flex justify-content-center">
        <div class="contact-header">
          <p class="mb-1 mb-md-3">Contact Us</p>
          <span class="line"></span>
        </div>
      </div>
    </div>
    <div class="row d-flex justify-content-center my-5">
      <div
        class="col-11 d-md-flex flex-md-row justify-content-md-between align-items-md-center"
      >
        <div class="col-md-7 col-12 pr-md-5 px-1">
          <div class="d-flex justify-content-between">
            <div class="text-container">
              <p class="contact-text text-nowrap">
                <a href="tel:+902125148090"
                  ><span class="contact-icon">T</span>+90 212 514 80 80
                </a>
              </p>
            </div>
            <div class="text-container text-nowrap">
              <p class="contact-text">
                <a href="tel:+905382976373">
                  <span class="contact-icon">W</span>+90 538 297 63 73
                </a>
              </p>
            </div>
          </div>
          <div class="d-flex justify-content-between pb-md-5">
            <div class="text-container">
              <p class="contact-text text-nowrap">
                <a href="tel:902122100606">
                  <span class="contact-icon">F</span>+90 212 210 06 06
                </a>
              </p>
            </div>
            <div class="text-container">
              <p class="contact-text text-nowrap text-truncate">
                <a href="mailto:info@kucukaslantekstil.com">
                  <span class="contact-icon">E</span>info@kucukaslantekstil.com
                </a>
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
          <b-form @submit="onSubmit">
            <b-form-group label="Name & Surname">
              <b-form-input
                v-model="form.fullName"
                type="text"
                required
                class="form-input"
              />
            </b-form-group>
            <b-form-group label="E-mail">
              <b-form-input
                v-model="form.email"
                type="email"
                required
                class="form-input"
              />
            </b-form-group>
            <b-form-group label="Message">
              <b-form-textarea
                v-model="form.message"
                required
                rows="4"
                class="form-input"
              />
            </b-form-group>
            <div class="d-flex justify-content-end align-items-center">
              <b-button
                :disabled="loading"
                class="input-submit-button"
                type="submit"
              >
                Send
              </b-button>
            </div>
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
      loading: false,
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
      const { fullName, email, message } = this.form
      if (!fullName || !email || !message) return
      this.loading = true
      setTimeout(() => {
        this.loading = false
      }, 1000)
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
.contact-text a {
  text-decoration: none;
  color: black;
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
  height: 50px;
  width: 145px;
  font-size: 18px;
  background: #000000;
  border-radius: 25px;
  line-height: 1;
}
.form-group,
.form-input {
  font-size: 24px;
}
@media screen and (max-width: 768px) {
  .input-submit-button {
    font-size: 12px;
    width: 67px;
    height: 28px;
  }
  .contact-icon,
  .contact-text {
    font-size: 12px;
  }
  .contact-icon {
    width: 11px;
  }
  .form-group,
  .form-input {
    font-size: 14px;
    width: 100%;
  }
  .form-input:not(textarea) {
    height: 25px;
  }
  .contact-header {
    font-size: 18px;
  }
  .text-container {
    width: 129px;
  }
}
</style>
