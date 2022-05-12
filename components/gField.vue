<template>
  <div class="grid">
      
    <div v-for="row in 6" :key="row" class="grid_row">
      <div v-for="(val, index) in 5" :key="index" class="grid-item"></div>
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

.grid_row {
  display: flex;
  flex-direction: row;
  align-items: center;
  column-gap: 10px;
}

.grid-item {
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

.grid-item:hover {
  transform: scale(1.1);
}
</style>