<template>
  <div class="grid">
    
    <div v-for="row in 6" :key="row" class="grid-row">
      <div v-for="(cell, index) in 5" :key="index" class="grid-cell"></div>
    </div>

  </div>
</template>

<script>
export default {
  name: "gField",
};
</script>

<style scoped>
.grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 10px;
}

.grid-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  column-gap: 10px;
}

.grid-cell {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;
  border: 1px solid var(--Grey);
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.2s;
}

.grid-cell:hover {
  transform: scale(1.1);
}
</style>