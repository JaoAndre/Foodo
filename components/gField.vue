<template>
  <div class="grid">

    <div v-for="(row, index) in grid" :key="index + '_row'" class="grid_row">
      {{ index }}
      <div
        v-for="(cell, index) in row"
        :key="index + '_cell'"
        class="grid_cell font-p"
      >
        {{ cell }}
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "gField",
  data() {
    return {
      grid: [
        ["", "", "", "", ""],
        ["", "", "", "", ""],
        ["", "", "", "", ""],
        ["", "", "", "", ""],
        ["", "", "", "", ""],
        ["", "", "", "", ""],
      ],
    };
  },
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

.grid_cell {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;
  border: 2px solid var(--Black);
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.2s;
}

.grid_cell:hover {
  transform: scale(1.1);
}
</style>