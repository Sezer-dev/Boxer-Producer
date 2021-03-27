<template>
  <div id="about" class="container-fluid about-container">
    <div class="row d-flex justify-content-center">
      <div
        class="col-11 d-flex flex-column align-items-md-end align-items-center"
      >
        <div class="m-3">
          <h1 class="about-title m-0">About</h1>
          <span class="red-line"></span>
        </div>
      </div>
    </div>

    <div class="row d-flex justify-content-center">
      <div
        class="col-11 d-flex justify-content-md-between justify-content-center align-items-center pb-2 pt-2 pb-md-5"
      >
        <div class="col-md-6 d-md-block d-none">
          <img
            class="boxer-sitting"
            src="~/assets/images/boxer-sitting.jpg"
            alt="Boxer"
          />
        </div>
        <div class="col-md-6 col-12 about-text">
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
export default {
  name: "About",
}
</script>

<style scoped>
.about-container {
  background-color: #f4f4f4;
}
.boxer-sitting {
  height: 389px;
  width: 584px;
  filter: grayscale(1);
  transition: all 0.5s ease-in-out;
}
.boxer-sitting:hover {
  filter: grayscale(0);
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
@media screen and (max-width: 768px) {
  .about-title {
    font-size: 24px;
    letter-spacing: 2px;
  }
  .about-text {
    font-size: 14px;
  }
}
@media screen and (min-width: 1440px) {
  .about-container {
    background-color: white;
  }
}
@media screen and (max-width: 1024px) {
  .boxer-sitting {
    width: 400px;
    object-fit: cover;
    height: 300px;
  }
  .about-text {
    font-size: 14px;
    object-fit: cover;
    object-position: 52% 0;
  }
}
</style>
