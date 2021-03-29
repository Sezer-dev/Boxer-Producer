<template>
  <div class="container-fluid my-5">
    <div class="row d-flex justify-content-center align-items-center brand-row">
      <div class="col-11 d-md-flex flex-md-row">
        <div
          class="col-md-5 col-12 d-flex justify-content-md-start justify-content-center mb-3 mb-md-0"
        >
          <img
            class="boxer-front"
            src="~/assets/images/boxer-front.jpg"
            alt="White Boxer"
          />
        </div>
        <div class="col-md-7 col-12">
          <div class="brand-title">
            <p class="text-center text-md-left">
              The Biggest Boxershort Manufacturer in
              <span class="text-alert">Turkey.</span>
            </p>
          </div>
          <div class="brand-text">
            <p>
              We are one of the companies that exports the high volume
              boxershorts from Turkey.
            </p>
            <p>
              Custom Design, Custom ideas; open for every entrepreneur
              individual/companies with reasonable Minimum Order Quantity.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Brand",
}
</script>

<style scoped>
.boxer-front {
  width: 343px;
  height: 437px;
}
.text-alert {
  color: #d81a04;
}
.brand-title p {
  font-size: 48px;
}
.brand-text p {
  font-size: 24px;
}
@media screen and (max-width: 768px) {
  .brand-title p {
    font-size: 24px;
  }
  .brand-text p {
    font-size: 14px;
  }
  .boxer-front {
    width: 186px;
    height: 237px;
  }
}
</style>
