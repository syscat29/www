<script setup>
  import ArrowRight from "../icons/ArrowRight.vue"

  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      default: null,
    },
  })
</script>

<template>
  <article>
    <img v-if="image" :src="image" :alt="name" />
    <img v-else src="/projects/default.png" :alt="name" />
    <div>
      <h3>{{ name }}</h3>
      <p>{{ description }}</p>
    </div>
    <ArrowRight size="16" />
  </article>
</template>

<style scoped>
  article {
    background-color: transparent;
    display: flex;
    align-items: center;
    padding: 1rem 0.750rem;
    border-radius: 8px;
    transition: all 0.3s ease-in-out;
    border: 1px solid #252525;

    img {
      align-self: start;
      margin-right: 0.5rem;
      height: 24px;
      width: 24px;
    }

    svg {
      margin-left: auto;
      transition: all 0.3s ease-in-out;
    }

    &:hover {
      background-color: #191919;

      svg {
        transform: rotate(-45deg);
      }
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
</style>
