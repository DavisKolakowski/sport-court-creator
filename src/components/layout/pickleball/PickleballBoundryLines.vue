<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <g id="Pickleball_Sidelines">
      <line 
        id="Pickleball-Sideline-Bottom" 
        x1="948.8" 
        y1="504.59" 
        x2="345.8" 
        y2="504.59" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
      <line 
        id="Pickleball-Sideline-Top" 
        x1="345.8" 
        y1="228.59" 
        x2="948.75" 
        y2="229.14" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
    </g>
    <g id="Pickleball_Center-Lines">
      <line 
        id="Pickleball_Center-Line-Left" 
        x1="345.8" 
        y1="366.59" 
        x2="548.4" 
        y2="366.59" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
      <line 
        id="Pickleball_Center-Line-Right" 
        x1="746.15" 
        y1="366.59" 
        x2="948.75" 
        y2="366.59" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
    </g>
    <g id="Pickleball_Baselines">
      <line 
        id="Pickleball_Baseline-Left" 
        x1="345.8" 
        y1="504.59" 
        x2="345.8" 
        y2="228.19" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="4.64" 
      />
      <line 
        id="Pickleball_Baseline-Right" 
        x1="948.75" 
        y1="505.34" 
        x2="948.75" 
        y2="229.14" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
    </g>
    <g id="Pickleball_Non-Volley-Lines">
      <line 
        id="Pickleball_Non-Volley-Line-Left" 
        x1="548.45" 
        y1="228.19" 
        x2="548.4" 
        y2="504.59" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="3.28" 
      />
      <line 
        id="Pickleball_Non-Volley-Line-Right" 
        x1="746.15" 
        y1="504.59" 
        x2="746.15" 
        y2="228.19" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="4.64" 
      />
    </g>
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PickleballBoundryLines",
  props: {
    lineColor: {
      type: String,
      default: "#FFFFFF"
    }
  },
  mounted() {
    this.$el.querySelectorAll('*').forEach((el: HTMLElement) => {
      if (el.hasAttribute('stroke')) {
        el.setAttribute('stroke', this.lineColor);
      }
    });
  }
});
</script>

<style scoped>
</style>
