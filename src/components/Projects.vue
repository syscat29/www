<script setup>
  import ProjectCard from "./ProjectCard.vue";
  import { projects } from "../data/projects";
</script>

<template>
  <section>
    <h2>// Projects</h2>
    <div class="projects">
      <ProjectCard
        v-for="{ name, description, tech, url } in projects"
        :name="name"
        :description="description"
        :tech="tech"
        :url="url"
      />
    </div>
  </section>
</template>

<style scoped>
  .projects {
    display: grid;
    /*grid-template-columns: repeat(auto-fit, minmax(340px, 3fr));*/
    grid-template-columns: 1fr;

    @media (min-width: 768px) {
      /*grid-template-columns: repeat(3, 1fr);*/
      grid-template-columns: 1fr;
    }
  }
</style>
