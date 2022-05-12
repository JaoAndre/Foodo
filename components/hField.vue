<template>
  <header>

    <h1 class="font-x">Foodo</h1>
    <div class="buttons">
      <button class="font-p">How to Play</button>
      <button class="font-p">Settings</button>
      <button class="font-p">Statistics</button>
    </div>

  </header>
</template>

<script>
export default {
  name: "hField",
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.buttons button {
  background: none;
  margin-left: 20px;
  cursor: pointer;
  transition: all 0.2s;
}

.buttons button:hover {
  transform: scale(1.1);
}
</style>