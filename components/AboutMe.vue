<template>
  <div class="about-me">
    <h2>About Me</h2>
    <div class="content">
      <img src="/images/john-doe.jpg" alt="John Doe" class="profile-picture">
      <div class="bio">
        <p>
          Hello! I'm John Doe, a passionate Full Stack Web Developer with over 5 years of experience in creating robust and scalable web applications.
        </p>
        <p>
          I specialize in JavaScript technologies, particularly Vue.js and Node.js. I'm also experienced with cloud platforms like AWS and have a strong foundation in database design and management.
        </p>
        <p>
          When I'm not coding, you can find me hiking in the mountains or experimenting with new recipes in the kitchen. I believe in continuous learning and am always excited to take on new challenges in the ever-evolving world of web development.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe'
}
</script>

<style scoped>
.about-me {
  max-width: 800px;
  margin: 0 auto;
}

.content {
  display: flex;
  align-items: flex-start;
  gap: 20px;
}

.profile-picture {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
}

.bio p {
  margin-bottom: 15px;
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
    align-items: center;
  }
}
</style>