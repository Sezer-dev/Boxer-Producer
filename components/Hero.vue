<template>
  <div class="container">
    <div class="row d-flex align-items-center">
      <div class="col-md-8">
        <p class="hero-text w-100">
          We design the most comfortable men’s
          <span class="text-alert">underwear.</span>
        </p>
      </div>
      <div class="col-md-4">
        <img
          class="hero-image"
          src="~/assets/images/full-body.jpg"
          alt="Boxer"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
}
</script>

<style scoped>
.hero-image {
  width: 466px;
  height: 463px;
}
.hero-text {
  font-size: 64px;
  letter-spacing: 4px;
  line-height: 82px;
  text-shadow: 4px 6px 4px rgba(0, 0, 0, 0.1);
}
.text-alert {
  color: #d81a04;
}
</style>
