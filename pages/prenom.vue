<template>
  <div class="container">
    <div class="wrapper">
      <h1 class="candidats">Sélectionnez un candidat :</h1>
      <NuxtLink to="admis" class="text-wrapper">
        <div class="arrow-wrapper">
          <div class="arrow">
            <span class="arrow-span">➡️</span>
          </div>
          <h1>Guillaume Tonneau</h1>
          <h1 class="interrogation">?</h1>
        </div>
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

h1 {
  margin: 0 1rem;
  font-size: 7rem;
}

.wrapper h1.candidats {
  position: absolute;
  top: 2rem;
  left: 5rem;
  font-size: 5rem;
  cursor: default;
}
@media screen and (max-width: 1520px) {
  .wrapper h1 {
    font-size: 5rem;
  }
}

@media screen and (max-width: 950px) {
  .wrapper h1 {
    font-size: 3rem;
  }
}
</style>