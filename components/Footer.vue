<template>
  <footer class="container-fluid bg-white py-md-5 py-0 mt-md-5 mt-0">
    <div class="row d-flex justify-content-center footer-row">
      <div
        class="col-11 d-flex flex-md-row flex-column justify-content-center justify-content-md-between align-items-center"
      >
        <div class="py-2 py-md-0">
          <Logo />
        </div>
        <p class="font-weight-bold m-0 text-md-start text-center py-2 py-md-0">
          © Boxer Producer 2021 - All rights reserved.
        </p>
        <a href="https://kucukaslantekstil.com/" class="py-2 py-md-0">
          <img
            class="kucukaslantekstil-logo"
            src="~/assets/images/kucukaslan-master.png"
            alt="kucukaslantekstil logo"
          />
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
}
</script>

<style scoped>
.kucukaslantekstil-logo {
  height: auto;
  width: 172px;
}
</style>
