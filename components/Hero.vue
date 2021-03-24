<template>
  <div class="container">
    <div
      class="row d-flex align-items-center justify-content-between flex-nowrap"
    >
      <div class="col-md-8 col-7 p-md-2">
        <p class="hero-text w-100">
          We design the most comfortable men’s
          <span class="text-alert">underwear.</span>
        </p>
      </div>
      <img
        class="hero-image col-md-4 col-5 px-0 p-md-2"
        src="~/assets/images/full-body.jpg"
        alt="Boxer"
      />
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
  object-fit: cover;
  object-position: center;
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
@media screen and (max-width: 768px) {
  .hero-text {
    font-size: 32px;
    letter-spacing: 2px;
    line-height: 48px;
  }
  .hero-image {
    width: 154px;
    height: 295px;
  }
}
@media screen and (max-width: 390px) {
  .hero-image {
    width: 154px;
    height: 255px;
  }
  .hero-text {
    font-size: 24px;
    line-height: 38px;
  }
}
</style>
