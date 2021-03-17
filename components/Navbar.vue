<template>
  <div class="container mt-3 mb-5 navbar-container">
    <b-nav>
      <b-nav-item exact-active-class="active" class="nav-link" to="/"
        >HOME</b-nav-item
      >
      <b-nav-item exact-active-class="active" class="nav-link" to="#about"
        >ABOUT</b-nav-item
      >
      <b-nav-item exact-active-class="active" class="nav-link" to="#products"
        >WHAT WE PRODUCE</b-nav-item
      >
      <b-nav-item exact-active-class="active" class="nav-link" to="#contact"
        >CONTACT</b-nav-item
      >
    </b-nav>
  </div>
</template>

<script>
export default {
  name: "Navbar",
}
</script>

<style scoped>
ul li a {
  color: black !important;
  font-size: 18px;
}
.navbar-container {
  background-color: #ffffff;
}
.nav-link a {
  padding: 0;
  margin: 8px 16px;
}
.active {
  border-bottom: 2px solid #d81a04;
}
</style>
