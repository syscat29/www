<script setup>
  import Github from "../icons/Github.vue"
  import Linkedin from "../icons/Linkedin.vue"
</script>

<template>
  <header>
    <div class="profile">
      <!-- <img
        src="https://avatars.githubusercontent.com/u/60985614?v=4"
        alt="Avatar"
      /> -->
      <div>
        <h1>SYSCAT</h1>
        <p>Web Developer</p>
      </div>
    </div>

    <nav class="socials">
      <a href="/" target="_blank">
        <Github size="20" />
      </a>
    </nav>
  </header>
</template>

<style scoped>
  header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .profile {
    display: flex;
    gap: 1rem;
    align-items: center;

    img {
      height: 48px;
      width: 48px;
      border-radius: 100%;
    }

    h1 {
      color: var(--text-strong);
      font-weight: 700;
    }

    p {
      color: var(--text-muted);
      font-size: 15px;
    }
  }

  .socials {
    display: flex;

    a {
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 0.5rem;
      border-radius: 4px;
      color: var(--text-muted);
      transition: all 0.3s ease;

      &:hover {
        background-color: #ffffff15;
        color: var(--text-strong);
      }
    }
  }
</style>
