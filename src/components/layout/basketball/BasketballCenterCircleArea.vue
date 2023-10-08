<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
    <circle 
        id="Basketball_Center-Circle-Area" 
        cx="649.98" cy="367.58" r="77.14" 
        :fill="fillColor" 
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BasketballCenterCircleArea",
  props: {
    fillColor: {
      type: String,
      default: "#00558f"
    }
  }
});
</script>
