<template>
  <div class="container">
    <div class="wrapper">
      <NuxtLink to="admis" class="text-wrapper">
        <h1>Guillaume Tonneau</h1>
        <h1 class="interrogation">?</h1>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    TweenLite.to(".interrogation", 0.6, {
      rotation: 30,
      transformOrigin: "center bottom",
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

.wrapper {
  height: 100vh;
  background-color: var(--background);
  display: flex;
  justify-content: center;
  align-items: center;
}

.wrapper h1 {
  cursor: pointer;
}

.text-wrapper:hover {
  text-shadow: -1px -1px 0 var(--beige), 0 -1px 0 var(--beige),
    1px -1px 0 var(--beige), 1px 0 0 var(--beige), 1px 1px 0 var(--beige),
    0 1px 0 var(--beige), -1px 1px 0 var(--beige), -1px 0 0 var(--beige);
  color: var(--background);
}

.text-wrapper {
  display: flex;
}

h1 {
  margin: 0 1rem;
  font-size: 9rem;
}
</style>