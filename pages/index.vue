<template>
  <div>
    <section class="hero">
      <h1>John Doe</h1>
      <p>Full Stack Web Developer</p>
    </section>
    <section id="about">
      <AboutMe />
    </section>
    <section id="skills">
      <Skills />
    </section>
    <section id="projects">
      <Projects />
    </section>
    <section id="contact">
      <ContactInfo />
    </section>
  </div>
</template>

<script setup>
import AboutMe from '~/components/AboutMe.vue'
import Skills from '~/components/Skills.vue'
import Projects from '~/components/Projects.vue'
import ContactInfo from '~/components/ContactInfo.vue'

useHead({
  title: 'John Doe - Full Stack Web Developer',
  meta: [
    { name: 'description', content: 'Portfolio of John Doe, a Full Stack Web Developer specializing in Vue.js, Node.js, and cloud technologies.' }
  ]
})
</script>

<style scoped>
.hero {
  text-align: center;
  padding: 100px 20px;
  background-color: #f0f0f0;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}

.hero p {
  font-size: 1.5rem;
  color: #666;
}
</style>