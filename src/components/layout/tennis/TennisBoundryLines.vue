<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <g id="Tennis_Baselines">
      <line 
        id="Tennis_Baseline-Left" 
        x1="132.6" 
        y1="608.85" 
        x2="132.6" 
        y2="125.23" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
      <line 
        id="Tennis_Baseline-Right" 
        x1="1152.09" 
        y1="125.23" 
        x2="1152.09" 
        y2="608.85" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
    </g>
    <g id="Tennis_Doubles-Sidelines">
      <line 
        id="Tennis_Doubles-Sideline-Bottom" 
        x1="1152.09" 
        y1="608.85" 
        x2="132.6" 
        y2="608.85" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
      <line 
        id="Tennis_Doubles-Sideline-Top" 
        x1="132.6" 
        y1="125.23" 
        x2="1152.09" 
        y2="125.23" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
    </g>
    <g id="Tennis_Singles-Sidelines">
      <line 
        id="Tennis_Singles-Sideline-Bottom" 
        x1="1152.09" 
        y1="539.18" 
        x2="132.6" 
        y2="539.18" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
      <line 
        id="Tennis_Singles-Sideline-Top" 
        x1="132.6" 
        y1="196.23" 
        x2="1152.09" 
        y2="196.23" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
    </g>
    <g id="Tennis_Service-Lines">
      <line 
        id="Tennis_Service-Line-Right" 
        x1="919.99" 
        y1="196.23" 
        x2="919.99" 
        y2="537.86" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="7.07" 
      />
      <line 
        id="Tennis_Service-Line-Center" 
        x1="374.56" 
        y1="367.04" 
        x2="919.99" 
        y2="367.04" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="5" 
      />
      <line 
        id="Tennis_Service-Line-Left" 
        x1="374.56" 
        y1="537.86" 
        x2="374.56" 
        y2="196.23" 
        fill="none" 
        :stroke="lineColor" 
        stroke-miterlimit="10" 
        stroke-width="7.07" 
      />
    </g>
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TennisBoundryLines",
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