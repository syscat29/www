<script setup>
  import Codeberg from "@/icons/Codeberg.vue";
  import Github from "@/icons/Github.vue";
</script>

<template>
  <header>
    <div class="socials">
      <a href="https://github.com/syscat29" target="_blank">
        <span>GitHub</span>
        <Github size="20" />
      </a>
      <a href="https://codeberg.org/aevilcat" target="_blank">
        <span>Codeberg</span>
        <Codeberg size="20" />
      </a>
    </div>
    <div class="about">
      <span>₍^. .^₎⟆</span>
      <h1>Hey, I'm Angel</h1>
      <p>
        Passionate about building stuff whether it be applications, developer tools, APIs, etc. I'm
        eager to learn new things and I'm not afraid to explore new technologies.
      </p>
    </div>
  </header>
</template>

<style scoped>
  header {
    display: flex;
    flex-direction: column;
    border-bottom: 1px dashed var(--border);

    .socials {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      border-bottom: 1px dashed var(--border);

      a {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0.875rem;
        color: var(--text-secondary);
        transition: all 0.3s ease;
        border-left: 1px dashed var(--border);

        span {
          position: aboslute;
          width: 1px;
          height: 1px;
          overflow: hidden;
        }

        &:hover {
          background-color: rgba(255, 255, 255, 0.075);
          color: var(--text-primary);
        }
      }
    }

    .about {
      padding: 2rem;

      span {
        color: var(--text-primary);
        font-size: 1.5rem;
        margin-bottom: 1rem;
        display: block;
      }

      h1 {
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 1rem;
        color: var(--text-primary);
      }

      p {
        font-size: 0.875rem;
        line-height: 1.5rem;
        color: var(--text-faint);
      }
    }
  }
</style>
