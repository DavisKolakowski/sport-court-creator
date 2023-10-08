<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <rect 
        id="Pickleball_Service-Area-Left" 
        x="345.75" 
        y="228.19" 
        width="202.7" 
        height="275.7" 
        :fill="areaColor" 
    />
    <rect 
        id="Pickleball_Service-Area-Right" 
        x="746.1" 
        y="228.39" 
        width="202.7" 
        height="275.7" 
        :fill="areaColor" 
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PickleballServiceArea",
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
