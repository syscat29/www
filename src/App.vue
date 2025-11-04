<script setup>
  import Header from "./components/Header.vue"
</script>

<template>
  <main>
    <Header />
  </main>
</template>

<style global>
  @font-face {
    font-family: "Geist";
    font-display: swap;
    font-style: normal;
    font-weight: 100 900;
    src: url("/fonts/Geist.ttf"), format("truetype");
  }

  *,
  *::before,
  *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  h1,
  h2,
  h3 {
    font-weight: inherit;
    font-size: inherit;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  :root {
    --bg-primary: #0d0d0d;
    --bg-secondary: #141414;
    --text-primary: #f0f0f0;
    --text-muted: #c7c7c7;
    --text-faint: #b3b3b3;
    --text-strong: #ffffff;

    color-scheme: light dark;
    color: var(--text-muted);
    background-color: var(--bg-secondary);

    font-synthesis: none;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  body {
    font-family: "Geist", system-ui, Avenir, Helvetica, Arial, sans-serif;
    line-height: 1.5;
    font-weight: 400;
    font-size: 15px;
    min-height: 100dvh;
    display: flex;
    justify-content: center;
  }

  main {
    width: 100%;
    max-width: 672px;
    padding: 3rem 1rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    position: relative;
  }

  section {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    font-size: 15px;

    h2 {
      font-weight: 700;
      color: var(--text-strong);
    }
  }
</style>
