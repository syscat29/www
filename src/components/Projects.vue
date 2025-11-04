<script setup>
  import ProjectCard from "./ProjectCard.vue"
  import { projects } from "../data/projects"
</script>

<template>
  <section>
    <h2>Projects</h2>
    <div class="projects">
      <a v-for="project in projects" :href="project.url" target="_blank">
        <ProjectCard
          :name="project.name"
          :description="project.description"
          :image="project.image"
          :githubUrl="project.githubUrl"
          :liveUrl="project.liveUrl"
        />
      </a>
    </div>
  </section>
</template>

<style scoped>
  .projects {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
</style>
