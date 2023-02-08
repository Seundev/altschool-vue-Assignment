<template>
  <h1>color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import colorPickerGame from "../composables/colorPickerGame";
export default {
  setup() {
    const { colors, message, matchColor} = colorPickerGame();
    return { colors, message, matchColor };
  },
};  
</script>

<style></style>
