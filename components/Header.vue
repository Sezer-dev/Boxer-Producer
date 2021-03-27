<template>
  <div
    class="container-fluid header-container d-flex flex-column align-items-start"
  >
    <div
      class="container d-flex justify-content-between align-items-center py-md-4 py-2"
    >
      <Logo />
      <nuxt-link
        to="#contact"
        class="contact-button border-0 text-decoration-none d-md-flex d-none justify-content-center align-items-center"
        >CONTACT US</nuxt-link
      >
      <b-navbar toggleable="md" class="d-md-none d-flex">
        <b-navbar-toggle target="toggle-nav"></b-navbar-toggle>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
}
</script>

<style>
.header-container {
  border-bottom: 1px solid #e5e5e5;
}

.contact-button {
  background-color: #000000;
  border-radius: 25px;
  height: 50px;
  width: 200px;
  color: white;
}
.contact-button:hover {
  color: white;
}
</style>
