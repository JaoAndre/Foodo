<template>
  <main>

    <section>
      <hField />
      <gField />
      <kField />
    </section>

  </main>
</template>

<script>
export default {
  name: "index",
};
</script>

<style scoped>
main {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

section {
  width: 700px;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>