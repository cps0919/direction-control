<template>
  <DirectionControl @direction="directionClick" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import DirectionControl from "@/components/direction.vue";
export default defineComponent({
  name: "App",
  components: {
    DirectionControl,
  },
  setup() {
    const directionClick = (e: { mouse: string; direction: number }) => {
      console.log(e);
    };
    return {
      directionClick,
    };
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
