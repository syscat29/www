<script setup>
  import ProjectCard from "./ProjectCard.vue";
  import { projects } from "../data/projects";
</script>

<template>
  <section>
    <h2>Projects</h2>
    <div class="projects">
      <ProjectCard
        v-for="project in projects"
        :name="project.name"
        :description="project.description"
        :icon="project.icon"
        :githubUrl="project.githubUrl"
        :url="project.url"
      />
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
