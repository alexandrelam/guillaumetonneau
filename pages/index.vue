<template>
  <div class="container">
    <h1 class="header1">Paris - Dauphine</h1>
    <div class="center">
      <h1 class="header2">Master Management de</h1>
      <h1 class="header3">l'innovation</h1>
    </div>
    <NuxtLink to="prenom">
      <div class="arrow-wrapper">
        <div class="header4 arrow">
          <span class="arrow-span">➡️</span>
        </div>
        <h1 class="header4 button">Admission 2021</h1>
      </div>
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
  text-align: center;
}

h1 {
  margin: 0 2rem;
  font-size: 7rem;
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

.arrow-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
}

.arrow-span {
  animation: 0.5s linear 0.5s infinite alternate slidein;
  left: 2.3em;
  font-size: 5rem;
}

@keyframes slidein {
  from {
    margin-left: 5%;
    width: 5%;
  }

  to {
    margin-left: 0%;
    width: 5%;
  }
}

.button:hover {
  text-shadow: -1px -1px 0 var(--beige), 0 -1px 0 var(--beige),
    1px -1px 0 var(--beige), 1px 0 0 var(--beige), 1px 1px 0 var(--beige),
    0 1px 0 var(--beige), -1px 1px 0 var(--beige), -1px 0 0 var(--beige);
  color: var(--background);
}

.header4 {
  margin-top: 5rem;
}

@media screen and (max-width: 1520px) {
  .container h1 {
    font-size: 5rem;
  }
}

@media screen and (max-width: 950px) {
  .container h1 {
    font-size: 3rem;
  }
}
</style>
