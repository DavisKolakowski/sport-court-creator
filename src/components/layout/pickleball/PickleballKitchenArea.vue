<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <rect 
        id="Pickleball_Kitchen" 
        x="548.4" 
        y="228.59" 
        width="197.7" 
        height="274.9" 
        :fill="areaColor" 
      />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PickleballKitchenArea",
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
