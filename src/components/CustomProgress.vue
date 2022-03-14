<template>
  <div class="custom-progress-bar">
    <div :style="computedStyle" />
  </div>
</template>
<script>
import { defineComponent, ref, onMounted } from "vue";

export default defineComponent({
  name: "CustomProgress",
  props: {
    percentage: {
      type: Number,
      required: true,
    },
  },
  setup(props) {
    const computedStyle = ref("");

    onMounted(() => {
      if (props.percentage) {
        console.log("onMounted", props.percentage);
        computedStyle.value = `width: ${props.percentage}%`;
      }
    });

    return {
      computedStyle,
    };
  },
});
</script>
<style lang="scss">
.custom-progress-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #ffffff50;
  width: 100%;
  height: 2px;
  div {
    background: white;
    height: 100%;
    width: 0;
  }
}
</style>
