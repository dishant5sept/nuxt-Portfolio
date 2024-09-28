<template>
  <div class="skills">
    <h2>Skills</h2>
    <div class="skill-categories">
      <div v-for="category in skillCategories" :key="category.name" class="skill-category">
        <h3>{{ category.name }}</h3>
        <ul>
          <li v-for="skill in category.skills" :key="skill">{{ skill }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skillCategories: [
        {
          name: 'Frontend',
          skills: ['HTML5', 'CSS3', 'JavaScript (ES6+)', 'Vue.js', 'Nuxt.js', 'React', 'Responsive Design']
        },
        {
          name: 'Backend',
          skills: ['Node.js', 'Express.js', 'Python', 'Django', 'RESTful APIs', 'GraphQL']
        },
        {
          name: 'Database',
          skills: ['MongoDB', 'PostgreSQL', 'MySQL', 'Redis']
        },
        {
          name: 'DevOps & Tools',
          skills: ['Git', 'Docker', 'AWS', 'CI/CD', 'Agile Methodologies', 'Jest', 'Webpack']
        }
      ]
    }
  }
}
</script>

<style scoped>
.skills {
  max-width: 800px;
  margin: 0 auto;
}

.skill-categories {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}

.skill-category h3 {
  margin-bottom: 10px;
  color: #007bff;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background-color: #f0f0f0;
  margin: 5px 0;
  padding: 5px 10px;
  border-radius: 5px;
  font-size: 0.9em;
}
</style>