<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <rect 
        id="Basketball_Three-Second-Area-Right" 
        x="1015.63" 
        y="290.7" 
        width="245.02" 
        height="155.7" 
        :fill="areaColor" 
    />
    <rect 
        id="Basketball_Three-Second-Area-Left" 
        x="38.18" 
        y="290.1" 
        width="245.02" 
        height="155.7" 
        :fill="areaColor" 
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BasketballThreeSecondArea",
  props: {
    areaColor: {
      type: String,
      default: "#FFFFFF"
    }
  },
  mounted() {
    this.$el.querySelectorAll('*').forEach((el: HTMLElement) => {
      if (el.hasAttribute('fill')) {
        el.setAttribute('fill', this.areaColor);
      }
    });
  }
});
</script>
