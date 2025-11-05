<script setup>
  import Codeberg from "@/icons/Codeberg.vue"
  import Github from "@/icons/Github.vue"
</script>

<template>
  <header>
    <div class="profile">
      <!-- <img src="https://avatars.githubusercontent.com/u/60985614?v=4" alt="Avatar" /> -->
      <div>
        <h1>Angel</h1>
        <p>@sachellein</p>
      </div>
    </div>

    <nav>
      <a href="https://github.com/syscat29" target="_blank">
        <Github size="20" />
      </a>
      <a href="https://codeberg.org/aevilcat" target="_blank">
        <Codeberg size="20" />
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
        font-size: 1.25rem;
      }

      p {
        color: var(--text-muted);
        font-size: 15px;
      }
    }

    nav {
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
  }
</style>
