<template>
  <q-page class="product-page-wrapper">
    <Header />
    <custom-carousel />
    <p class="product-gmp">£251.99 GBP</p>
    <p class="product-title">Vintage Oversized Pattern Fleece</p>
    <p class="product-description">
      This updated unisex essential fits like a well loved favorite. Super soft
      cotton and excellent quality print makes one to fall in love with it over
      and over again.
    </p>
    <div style="color: #fff" class="product-property">
      <q-btn icon="info" label="view details" class="no-shadow" />
      <q-btn icon="local_shipping" label="FREE SHIPPING" class="no-shadow" />
      <q-btn icon="shield" label="BUYER PROTECTION" class="no-shadow" />
      <q-btn icon="chat_bubble" label="MAKE OFFER" class="no-shadow" />
    </div>
    <div class="flex justify-between product-btn-group">
      <q-btn label="Make offer" no-caps class="product-offer-btn" />
      <q-btn label="Buy item" no-caps class="product-buy-btn" />
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import Header from "components/Header.vue";
import CustomCarousel from "components/CustomCarousel.vue";

export default defineComponent({
  name: "ProductPage",
  components: {
    Header,
    CustomCarousel,
  },
});
</script>

<style lang="scss">
.product-page-wrapper {
  margin-left: auto;
  max-width: 404px;
  margin-right: auto;
  padding-left: 24px;
  padding-right: 24px;
}

.q-carousel__arrow .q-btn {
  background: rgba(0, 0, 0, 0.4);
}

.q-carousel__arrow .q-icon {
  font-size: 16px;
}
.product-gmp {
  font-family: "Nexa Regular";
  font-weight: 800;
  font-size: 12px;
  line-height: 16px;
  color: #ffffff;
  margin-top: 16px;
  margin-bottom: 8px;
}

.product-title {
  font-family: "Migra Medium";
  font-weight: 500;
  font-size: 40px;
  line-height: 48px;
  color: #ffffff;
  margin-bottom: 8px;
}

.product-description {
  font-family: "Nexa Regular";
  font-size: 14px;
  line-height: 20px;
  font-weight: 700;
  color: rgba(255, 255, 255, 0.6);
}

.product-property {
  margin-top: 16px;
  margin-bottom: 16px;
  display: inline-grid;
  grid-template-columns: 50% 50%;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  border-left: 1px solid rgba(255, 255, 255, 0.1);
  width: 100%;
}

.product-property > button {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  border-right: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 0;
  font-size: 10px;
  font-family: "NexaHeavy";
  font-weight: 800;
  line-height: 12px;
  padding-top: 17px;
  padding-bottom: 18px;
  .q-btn:before {
    box-shadow: none !important;
  }
}

.product-property > button .q-icon {
  font-size: 12px;
}

.product-btn-group {
  padding-bottom: 51px;
}

.product-offer-btn {
  background: rgba(255, 255, 255, 0.1);
  color: #e0cbfb;
  font-family: "Nexa Regular";
  font-size: 16px;
  line-height: 21px;
  padding: 17px 16px 18px;
  font-weight: 900;
}

.product-buy-btn {
  background: #e0cbfb;
  color: #000000;
  font-family: "Nexa Regular";
  font-size: 16px;
  line-height: 21px;
  padding: 17px 77px 18px;
  font-weight: 900;
}

@media (max-width: $breakpoint-xs-max) {
  .product-gmp {
    margin-bottom: 3px;
  }

  .product-title {
    font-weight: 500;
    font-size: 30px;
    line-height: 36px;
    color: #ffffff;
  }

  .product-offer-btn {
    display: none;
  }

  .product-buy-btn {
    width: 100%;
  }

  .q-carousel__arrow .q-btn {
    display: none;
  }

  .product-btn-group {
    padding-bottom: 24px;
  }
}
</style>
