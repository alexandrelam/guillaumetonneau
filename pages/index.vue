<template>
  <div class="container">
    <h1 class="header1">Paris - Dauphine</h1>
    <div class="center">
      <h1 class="header2">Master Management de</h1>
      <h1 class="header3">l'innovation</h1>
    </div>
    <NuxtLink to="prenom">
      <h1 class="header4 button">Admission 2021</h1>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$nextTick(() => {
      // When using $refs, must wait for nextTick
      const tl = this.$gsap.timeline();
      tl.from(".header1", {
        y: -90,
        opacity: 0,
        duration: 0.4,
      }); // With css selector
      tl.from(".header2", {
        y: -90,
        opacity: 0,
        duration: 0.4,
      }); // With css selector
      tl.from(".header3", {
        y: -90,
        opacity: 0,
        duration: 0.4,
      }); // With css selector
      tl.from(".header4", {
        y: -90,
        opacity: 0,
        duration: 0.4,
      }); // With css selector
    });
  },
};
</script>

<style>
* {
  font-family: "Cabin";
  --beige: #f0ece2;
  --background: #151515;
}

a {
  text-decoration: none;
  color: var(--beige);
}

body {
  margin: 0;
  color: var(--beige);
}

h1 {
  margin: 0 2rem;
  font-size: 9rem;
  cursor: default;
}

.container {
  height: 100vh;
  background-color: var(--background);
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.center {
  margin: 3rem 0;
}

.button {
  cursor: pointer;
  transition-duration: 1000;
}

.button:hover {
  text-shadow: -1px -1px 0 var(--beige), 0 -1px 0 var(--beige),
    1px -1px 0 var(--beige), 1px 0 0 var(--beige), 1px 1px 0 var(--beige),
    0 1px 0 var(--beige), -1px 1px 0 var(--beige), -1px 0 0 var(--beige);
  color: var(--background);
}
</style>
