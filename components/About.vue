<template>
  <div id="about" class="container-fluid about-container">
    <div
      class="row col-md-10 offset-1 d-flex justify-content-between pt-4 pb-5"
    >
      <div class="col-md-12 d-flex flex-column align-items-end">
        <div class="m-3">
          <h1 class="about-title m-0">About</h1>
          <span class="red-line"></span>
        </div>
      </div>
      <div
        class="col-md-12 d-flex justify-content-between align-items-center pt-2 pb-5"
      >
        <div class="col-md-5">
          <img
            class="boxer-sitting"
            src="~/assets/images/boxer-sitting.jpg"
            alt="Boxer"
          />
        </div>
        <div class="col-md-5 about-text">
          <p>
            Founded in 1924 by Hüseyin Küçükaslan, Kucukaslan Tekstil company in
            a short period of time became Turkey's leading brand in underwear
            clothing.
          </p>
          <p>
            Manufacturer of wool, thermal and cotton underwear, shapers, bamboo
            shapers, socks, pajamas and boxer types & with up to 30 knitting
            machines, producing its own needs of fabrics in house.
          </p>
          <p>
            With its employees and executives who have adopted innovation;
            working without sacrificing customer satisfaction and quality is the
            fundamentals of the company's understanding of service.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.about-container {
  background-color: #f4f4f4;
}
.boxer-sitting {
  height: 389px;
  width: auto;
  filter: grayscale(1);
}
.boxer-sitting:hover {
  filter: grayscale(0);
  transition: all 0.2s;
}
.red-line {
  border-bottom: 4px solid #d81a04;
  display: block;
}
.about-title {
  font-size: 48px;
  letter-spacing: 4px;
}
.about-text {
  font-size: 18px;
}
</style>
