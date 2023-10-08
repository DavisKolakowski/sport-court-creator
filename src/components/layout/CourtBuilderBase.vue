<template>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
      <rect
        :x="2.64"
        :y="2.64"
        :width="1290.99"
        :height="735.99"
        :fill="baseColor"
        :stroke="fenceColor"
        :stroke-miterlimit="10"
        :stroke-width="5.29"
      />
    </svg>
  </template>
  
  <script lang="ts">
  import { ref, defineComponent } from "vue";
  
  export default defineComponent({
    name: "CourtBuilderBase",
    props: {
      baseColor: {
        type: String,
        default: "#6c6d6f"
      },
      fenceColor : {
        type: String,
        default: "#241f20"        
      }
    }
  });
  </script>