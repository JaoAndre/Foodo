<template>
  <div class="keyboard">

    <div
      v-for="(row, index) in keyboard"
      :key="index + '_row'"
      class="keyboard_row"
    >
      {{ index }}
      <div v-for="letter in row" :key="letter" class="nKey font-p">
        {{ letter }}
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "kField",
  data() {
    return {
      keyboard: [
        ["Q", "W", "E", "R", "T", "Y", "U", "I", "O", "P"],
        ["A", "S", "D", "F", "G", "H", "J", "K", "L"],
        ["Z", "X", "C", "V", "B", "N", "M"],
      ],
    };
  },
};
</script>

<style scoped>
.keyboard {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  row-gap: 10px;
}

.keyboard_row {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 100%;
  column-gap: 10px;
}

.nKey {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;
  background: var(--Grey);
  border: 2px solid var(--Black);
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.2s;
}

.nKey:hover {
  transform: scale(1.1);
}
</style>