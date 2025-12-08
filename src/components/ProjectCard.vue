<script setup>
  import ArrowRight from "@/icons/ArrowRight.vue";

  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    language: {
      type: String,
    },
    url: {
      type: String,
      default: null,
    },
  });
</script>

<template>
  <a :href="url" target="_blank" nofollow noreferrer>
    <div class="project">
      <div class="project__info">
        <h3>{{ name }}</h3>
        <p>{{ description }}</p>
      </div>
      <div class="project__meta">
        <p>{{ language }}</p>
        <span :href="url">
          <ArrowRight size="16" />
        </span>
      </div>
    </div>
  </a>
</template>

<style scoped>
  a {
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    border-color: var(--border);
    border-style: dashed;
    border-width: 0;

    &:hover {
      background-color: rgba(255, 255, 255, 0.05);
    }

    &:not(:first-child) {
      border-top-width: 1px;
    }

    @media (min-width: 768px) {
      &:not(:first-child) {
        border-top-width: 0;
        border-left-width: 1px;
      }
    }

    .project {
      display: flex;
      flex-direction: column;
      padding: 1rem;
      gap: 1rem;
      height: 100%;

      &:hover {
        .project__meta span {
          transform: translateX(0);
          opacity: 1;
        }
      }

      .project__info {
        display: flex;
        gap: 0.5rem;
        flex-direction: column;

        h3 {
          color: var(--text-primary);
          font-weight: 600;
        }

        p {
          color: var(--text-faint);
          font-size: 0.875rem;
        }
      }

      .project__meta {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        gap: 0.25rem;
        margin-top: auto;

        p {
          font-size: 0.75rem;
          color: var(--text-muted);
          font-family: var(--font-mono);
          text-transform: capitalize;
        }

        span {
          color: var(--text-strong);
          opacity: 0;
          transition: all 0.2s ease-in-out;
          transform: translateX(-4px);
        }
      }
    }
  }
</style>
