<script setup>
  import Github from "@/icons/Github.vue"
  import ArrowExternal from "@/icons/ArrowExternal.vue"

  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      default: "/images/projects/default.png",
    },
    githubUrl: {
      type: String,
      default: null,
    },
    url: {
      type: String,
      default: null,
    },
  })
</script>

<template>
  <article class="project">
    <div class="project__meta">
      <img :src="icon" :alt="name" />
      <div>
        <h3>{{ name }}</h3>
        <p>{{ description }}</p>
      </div>
    </div>
    <div class="project__links">
      <a v-if="githubUrl" :href="githubUrl" target="_blank">
        <Github size="16" />
      </a>
      <a v-if="url" :href="url" target="_blank">
        <ArrowExternal size="16" />
      </a>
    </div>
  </article>
</template>

<style scoped>
  .project {
    background-color: #202020;
    display: flex;
    border-radius: 8px;
    transition: all 0.3s ease-in-out;

    .project__meta {
      display: flex;
      gap: 0.5rem;
      padding: 1rem 0.75rem;

      img {
        height: 24px;
        width: 24px;
      }

      h3 {
        color: var(--text-primary);
        font-weight: 500;
      }

      p {
        color: var(--text-faint);
        font-size: 14px;
      }
    }

    .project__links {
      padding: 0.75rem;
      margin-left: auto;
      display: flex;
      align-items: start;
      gap: 0.25rem;

      a {
        display: inline-flex;
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
