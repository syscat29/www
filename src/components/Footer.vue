<script setup>
  import ArrowExternal from "@/icons/ArrowExternal.vue"
</script>

<template>
  <footer>
    <p>&copy; Syscat</p>
    <p>
      <a href="https://github.com/syscat29/www" target="_blank">
        Source
        <ArrowExternal size="12" />
      </a>
    </p>
  </footer>
</template>

<style scoped>
  footer {
    margin-top: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;

    a {
      display: flex;
      align-items: center;
      gap: 0.25rem;
      transition: all 0.3s ease;

      &:hover {
        color: var(--text-strong);
      }
    }
  }
</style>
