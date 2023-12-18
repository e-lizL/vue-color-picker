<template lang="">
  <div class="color-picker-container">
    <h1>Color Picker</h1>
    <div class="color-box" :style="{ backgroundColor: selectedColor }">
      <p>Chosen Color: {{ selectedColor }}</p>
    </div>
    <label>Choose a Color:</label>
    <input type="color" v-model="selectedColor" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedColor: "#ffffff", //default color
    };
  },
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
}

h1 {
  color: rgb(64, 63, 63);
}

.color-picker-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  margin-top: 50px;
}

.color-box {
  width: 300px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 5px solid rgb(228, 226, 226);
  border-radius: 25px;
  margin-bottom: 25px;
  transition: 0.25s ease;
  color: rgb(122, 120, 120);
}

label {
  font-size: 1.5rem;
  color: rgb(64, 63, 63);
  margin-bottom: 10px;
}

input[type="color"] {
  border-radius: 10px;
  width: 75px;
  height: 50px;
  padding: 5px;
  border: 3px solid rgb(228, 226, 226);
}
</style>
