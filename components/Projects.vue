<template>
  <div class="projects">
    <h2>Projects</h2>
    <div class="project-grid">
      <div v-for="project in projects" :key="project.title" class="project">
        <img :src="project.image" :alt="project.title" class="project-image">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <div class="technologies">
          <span v-for="tech in project.technologies" :key="tech" class="tech-tag">{{ tech }}</span>
        </div>
        <a :href="project.link" target="_blank" rel="noopener noreferrer" class="project-link">View Project</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'E-commerce Platform',
          description: 'A fully responsive e-commerce website built with Vue.js and Nuxt.js, featuring user authentication, product catalog, shopping cart, and payment integration.',
          image: '/images/ecommerce-project.jpg',
          technologies: ['Vue.js', 'Nuxt.js', 'Node.js', 'Express', 'MongoDB'],
          link: 'https://github.com/johndoe/ecommerce-platform'
        },
        {
          title: 'Task Management App',
          description: 'A collaborative task management application with real-time updates, user roles, and project analytics. Built with React and Firebase.',
          image: '/images/task-management-app.jpg',
          technologies: ['React', 'Firebase', 'Redux', 'Material-UI'],
          link: 'https://github.com/johndoe/task-management-app'
        },
        {
          title: 'Weather Forecast Dashboard',
          description: 'A weather forecast dashboard that provides real-time weather data and 7-day forecasts for multiple locations. Utilizes a third-party weather API and features interactive charts.',
          image: '/images/weather-dashboard.jpg',
          technologies: ['Vue.js', 'Chart.js', 'OpenWeatherMap API', 'Geolocation API'],
          link: 'https://github.com/johndoe/weather-dashboard'
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects {
  max-width: 1200px;
  margin: 0 auto;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.project {
  background-color: #f9f9f9;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.project:hover {
  transform: translateY(-5px);
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.project h3 {
  margin: 15px;
}

.project p {
  margin: 0 15px 15px;
  font-size: 0.9em;
}

.technologies {
  margin: 0 15px 15px;
}

.tech-tag {
  display: inline-block;
  background-color: #007bff;
  color: white;
  padding: 3px 8px;
  border-radius: 3px;
  font-size: 0.8em;
  margin-right: 5px;
  margin-bottom: 5px;
}

.project-link {
  display: inline-block;
  margin: 15px;
  padding: 8px 15px;
  background-color: #007bff;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.project-link:hover {
  background-color: #0056b3;
}
</style>