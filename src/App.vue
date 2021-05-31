<template>
  <div id="app">
    <TheHeader />
    <main id="main">
      <router-view/>
    </main>
    <TheFooter />
  </div>
</template>

<script>

import TheHeader from '@/components/TheHeader'
import TheFooter from '@/components/TheFooter'

export default {
  components: {
    TheHeader,
    TheFooter
  }
}
</script>

<style>

:root {
  --roxo: #87f;
  --azul: #65d;
}

* {
  box-sizing: border-box;
}

body, ul, li, h1, h2, p {
  margin: 0px;
  padding: 0px;
}

ul {
  list-style: none;
}

body {
  font-family: "Arial", 'helvetica';
  color: #345;
  background: url("./assets/pattern.svg") repeat top;
}

a {
  color: #345;
  text-decoration: none;
}

img {
  max-width: 100%;
  display: block;
}

.btn {
  display: block;
  padding: 10px 30px;
  background: var(--roxo);
  color: #fff;
  text-align: center;
  font-size: 1rem;
  box-shadow: 0px 4px 8px rgba(30, 60, 90, 0.2);
  transition: all 0.3s;
  border: none;
  font-family: "Arial";
  cursor: pointer;
}

.btn:hover {
  background: var(--azul);
  transform: scale(1.1);
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

#main {
  flex: 1;
}
</style>
