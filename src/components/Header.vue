<template>
  <div class="product-mob-header-line">
    <custom-progress :percentage="50" />
    <custom-progress :percentage="0" />
    <custom-progress :percentage="0" />
    <custom-progress :percentage="0" />
  </div>
  <div class="flex flex-center header">
    <img src="../assets/images/sun.svg" />
    <span class="header-title"> DayBreak Vintage</span>
    <q-btn class="forward-btn">
      <q-avatar size="20px">
        <img src="../assets/images/share.svg" />
      </q-avatar>
    </q-btn>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import CustomProgress from "./CustomProgress.vue";

export default defineComponent({
  name: "Header",
  components: {
    CustomProgress,
  },
});
</script>

<style lang="scss">
.header {
  padding-top: 32px;
  padding-bottom: 16px;
  background: transparent;
  max-width: 356px;
}

.header-title {
  font-family: "Migra Medium";
  font-weight: 500;
  line-height: 29px;
  color: #ffffff;
  font-size: 24px;
  padding-left: 8px;
}

.forward-btn {
  margin-left: auto;
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.2);
}

.product-mob-header-line {
  display: none;
}

@media (max-width: $breakpoint-xs-max) {
  .product-mob-header-line {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding-top: 16px;
    background: transparent;
    & > div {
      width: 23%;
    }
  }
  .q-btn:before {
    box-shadow: none !important;
  }
  .header {
    padding-top: 16px;
  }
}
</style>
