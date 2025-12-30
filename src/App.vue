<script setup>
  import Header from "@/components/Header.vue";
  import Footer from "@/components/Footer.vue";
  import Projects from "@/components/Projects.vue";
  import Skills from "@/components/Skills.vue";
</script>

<template>
  <div class="container">
    <Header />
    <Projects />
    <Skills />
    <Footer />
  </div>
</template>

<style global>
  @font-face {
    font-family: "Geist";
    font-display: swap;
    font-style: normal;
    font-weight: 100 900;
    src: url("/fonts/Geist.ttf"), format("truetype");
  }

  @font-face {
    font-family: "Geist Mono";
    font-display: swap;
    font-style: normal;
    font-weight: 100 900;
    src: url("/fonts/GeistMono.ttf"), format("truetype");
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
  h3,
  h4 {
    font-weight: inherit;
    font-size: inherit;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  ::selection {
    background-color: #ffffff30;
    color: var(--text-primary);
  }

  :root {
    --font-sans: "Geist", system-ui, Avenir, Helvetica, Arial, sans-serif;
    --font-mono: "Geist Mono", monospace;

    --background: #000000;
    --text-primary: #ffffff;
    --text-secondary: #a3a3a3;
    --text-muted: #737373;
    --border: #262626;

    color: var(--text-secondary);
    background-color: var(--background);

    font-synthesis: none;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  body {
    font-family: var(--font-sans);
    line-height: 1.5;
    font-weight: 400;
    font-size: 16px;
    min-height: 100dvh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1rem;
  }

  @media (min-width: 768px) {
    body {
      padding: 2rem;
    }
  }

  @media (min-width: 1024px) {
    body {
      padding: 3rem;
    }
  }

  .container {
    width: 100%;
    display: flex;
    flex-direction: column;
    position: relative;
    max-width: 700px;
    border: 1px dashed var(--border);
  }

  section {
    border-bottom: 1px dashed var(--border);

    &:last-of-type {
      border-bottom: 0px;
    }

    h2 {
      border-bottom: 1px dashed var(--border);
      font-family: var(--font-mono);
      font-size: 0.6875rem;
      padding: 0.875rem;
      color: var(--text-secondary);
      text-transform: uppercase;
      letter-spacing: 2px;
    }
  }
</style>
