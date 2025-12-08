<script setup>
  import ArrowExternal from "@/icons/ArrowExternal.vue";
</script>

<template>
  <footer>
    <p>&copy; Syscat</p>
    <a href="https://github.com/syscat29/www" target="_blank">
      Source
      <ArrowExternal size="10" />
    </a>
  </footer>
</template>

<style scoped>
  footer {
    margin-top: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px dashed var(--border);
    padding: 0.5rem 1rem;
    font-family: var(--font-mono);
    font-size: 0.75rem;
    color: var(--text-muted);

    a {
      display: flex;
      align-items: center;
      gap: 0.25rem;
      transition: all 0.3s ease;

      &:hover {
        color: var(--text-primary);
      }
    }
  }
</style>
