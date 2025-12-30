<script setup>
  import { skills } from "../data/skills";
</script>

<template>
  <section>
    <h2>// Skills</h2>
    <div class="skills">
      <div class="skill__group" v-for="(skillList, skillName) in skills" :key="skillName">
        <h3>{{ skillName }}</h3>
        <ul>
          <li v-for="skill in skillList" :key="skill">
            {{ skill }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .skills {
    display: grid;
    grid-template-columns: 1fr;

    @media (min-width: 768px) {
      grid-template-columns: repeat(3, 1fr);
    }

    .skill__group {
      padding: 1rem;

      &:not(:first-child) {
        border-top: 1px dashed var(--border);
      }

      @media (min-width: 768px) {
        &:not(:first-child) {
          border-left: 1px dashed var(--border);
          border-top: none;
        }
      }

      h3 {
        font-size: 0.875rem;
        letter-spacing: 1px;
        /*font-weight: 500;*/
        color: var(--text-primary);
        margin-bottom: 0.5rem;
        text-transform: capitalize;
      }

      ul {
        padding: 0;
        margin: 0;
        list-style-position: inside;

        li {
          margin-bottom: 0.025rem;
          font-size: 0.75rem;
          letter-spacing: 1px;
        }
      }
    }
  }
</style>
