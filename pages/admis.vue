<template>
  <div class="container">
    <div class="wrapper">
      <h1 class="titre">Admis !</h1>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    gsap.from(".titre", 1.2, { scale: 0.3 });
    this.$confetti.start();
  },
};
</script>

<style>
* {
  font-family: "Cabin";
  --beige: #f0ece2;
  --background: #151515;
}

body {
  margin: 0;
  color: var(--beige);
}

.container {
  height: 100vh;
  background-color: var(--background);
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.wrapper {
  height: 100vh;
  background-color: var(--background);
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  margin: 0 2rem;
  font-size: 9rem;
  cursor: default;
}
</style>