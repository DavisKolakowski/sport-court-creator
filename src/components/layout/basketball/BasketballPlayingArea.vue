<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <rect 
        id="Basketball_Playing-Area" 
        x="37.3" 
        y="44.33" 
        width="1223.36" 
        height="644.33" 
        :fill="areaColor" 
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BasketballPlayingArea",
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
