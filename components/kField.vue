<template>
  <div class="keyboard">

    <div class="keyboard_row">
      <div v-for="letter in ['Q', 'W', 'E', 'R', 'T', 'Y', 'U', 'I', 'O', 'P']" :key="letter" class="nKey">{{ letter }}</div>
    </div>

    <div class="keyboard_row">
      <div v-for="letter in ['A', 'S', 'D', 'F', 'G', 'H', 'J', 'K', 'L']" :key="letter" class="nKey">{{ letter }}</div>
    </div>

    <div class="keyboard_row">
      <div v-for="letter in ['Z', 'X', 'C', 'V', 'B', 'N', 'M']" :key="letter" class="nKey" >{{ letter }}</div>
    </div>

  </div>
</template>

<script>
export default {
  name: "kField",
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
  border: 1px solid var(--Grey);
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.2s;
}

.nKey:hover {
  transform: scale(1.1);
}
</style>