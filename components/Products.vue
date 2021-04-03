<template>
  <div id="products" class="container-fluid my-3 py-3 my-md-5 py-md-5">
    <div class="row pb-5 d-flex justify-content-center">
      <div class="col-11 d-flex justify-content-center">
        <div>
          <p class="product-title m-0">What we produce?</p>
          <span class="red-line"></span>
        </div>
      </div>
    </div>
    <div class="row d-flex justify-content-center products-row">
      <div class="col-11 accordion-container">
        <div v-for="(accordion, index) of accordions" :key="index">
          <b-button
            v-b-toggle:[accordion.id+index]
            :class="{ expanded: accordion.expand }"
            class="accordion-button d-flex justify-content-between align-items-center shadow-none p-4"
          >
            {{ accordion.title }}
            <plus-icon v-if="!accordion.expand"></plus-icon>
            <dash-icon v-else></dash-icon>
          </b-button>
          <b-collapse
            :id="accordion.id + index"
            :key="index"
            accordion="products-accordion"
            class="accordion-text p-4"
            @hide="opening(index)"
            @show="closing(index)"
          >
            <div>
              <p v-for="(text, textIndex) of accordion.texts" :key="textIndex">
                {{ text }}
              </p>
            </div>
          </b-collapse>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { BIconPlus, BIconDash } from "bootstrap-vue"
export default {
  name: "Products",
  components: {
    "plus-icon": BIconPlus,
    "dash-icon": BIconDash,
  },
  data() {
    return {
      accordions: [
        {
          id: "cotton",
          title: "Men's Cotton Boxershorts",
          texts: [
            "One of the most common fabrics from which the biggest manufacturers produce their underwear in, cotton has become widely used in this industry for many reasons.",
            "It is natural and breathable; it is highly affordable and absorbent, perfect to keep user private areas safe and healthy. It is perfect in most of the cases, exceeding other fabrics in wearing conditions.",
            "However, textile experts advise those who tend to exercise a lot to ditch the old cotton briefs when working out and replace them with nylon/polyester ones. Since cotton absorbs quite well humidity, it will become easily impregnated with all the sweat resulting when working out, which is uncomfortable.",
          ],
          expand: false,
        },
        {
          id: "bamboo",
          title: "Men's Bamboo Boxershorts",
          texts: [
            "Our sustainable men's bamboo boxers are cut for comfort in our breathable and incredibly soft bamboo fabric.",
            "Maybe the most elegant fabric for underwear, it is amazing even for those with sensitive skin types.",
            "It is perfect. It is a cooling fabric, perfect for hot summer days.",
          ],
          expand: false,
        },
        {
          id: "modal",
          title: "Men's Modal Boxershorts",
          texts: [
            "Nothing beats this particular fabric in the softness department. And if nylon is not fit for you, this fabric might work wonders.",
            "It might not be the most appropriate to wear while working out, since it does not offer plenty of support, but under jeans or suit pants, it works great.",
            "Being so soft, boxer briefs in fabric are considerably more comfortable to wear than others are.",
          ],
          expand: false,
        },
      ],
    }
  },
  methods: {
    opening(index) {
      this.accordions[index].expand = !this.accordions[index].expand
    },
    closing(index) {
      this.accordions[index].expand = !this.accordions[index].expand
    },
  },
}
</script>

<style scoped>
.product-title {
  font-size: 36px;
}
.red-line {
  display: block;
  border-bottom: 4px solid #d81a04;
}
.accordion-container {
  border: 1px solid #e5e5e5;
  border-radius: 8px;
}
.accordion-button {
  background-color: white;
  color: #000000;
  width: 100%;
  border: none;
  border-bottom: 1px solid #e5e5e5;
  font-size: 18px;
}
.accordion-button:active {
  background-color: white !important;
  color: #000000 !important;
}
.expanded {
  color: #d81a04;
}
.accordion-text {
  font-size: 14px;
  transition: all 0.2s linear !important;
}
.accordion-text.collapse {
  opacity: 0 !important;
}
.accordion-text.collapse.show {
  opacity: 1 !important;
}
@media screen and (max-width: 768px) {
  .product-title {
    font-size: 18px;
  }
  .accordion-text {
    font-size: 12px;
  }
  .accordion-button {
    font-size: 14px;
  }
  .products-row {
    margin-right: 0;
    margin-left: 0;
  }
}
</style>

<style>
.collapsing {
  transition: none !important;
}
</style>
