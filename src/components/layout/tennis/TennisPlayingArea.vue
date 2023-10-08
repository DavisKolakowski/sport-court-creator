<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <rect 
        id="Tennis_Playing-Area" 
        x="134.67" 
        y="125.48" 
        width="1019" 
        height="483" 
        :fill="areaColor" 
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TennisPlayingArea",
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
