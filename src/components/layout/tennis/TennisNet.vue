<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <g id="Tennis_Net">
      <line 
        id="Tennis_Net-Webbing" 
        x1="647.73" 
        y1="105.89" 
        x2="647.73" 
        y2="639.69" 
        fill="none" 
        stroke="#fbfcfc" 
        stroke-dasharray="0 0 0 0 0 0 13 21" 
        stroke-miterlimit="10" 
        stroke-width="5.36" 
      />
      <g id="Tennis_Posts">
        <circle 
            id="Tennis_Post-Top" 
            cx="647.73" 
            cy="93.09" 
            r="12.79" 
            fill="#fbfcfc" 
        />
        <circle 
            id="Tennis_Post-Bottom" 
            cx="647.73" 
            cy="639.69" 
            r="12.79" 
            fill="#fbfcfc" 
        />
      </g>
    </g>
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TennisNet"
});
</script>
