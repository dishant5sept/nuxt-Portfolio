<template>
  <div class="contact-info">
    <h2>Contact Me</h2>
    <div class="contact-content">
      <div class="contact-details">
        <h3>Get in Touch</h3>
        <p>I'm always open to new opportunities and collaborations. Feel free to reach out!</p>
        <ul>
          <li><strong>Email:</strong> john.doe@example.com</li>
          <li><strong>Phone:</strong> +1 (123) 456-7890</li>
          <li><strong>Location:</strong> San Francisco, CA</li>
        </ul>
        <div class="social-links">
          <a href="https://github.com/johndoe" target="_blank" rel="noopener noreferrer">GitHub</a>
          <a href="https://linkedin.com/in/johndoe" target="_blank" rel="noopener noreferrer">LinkedIn</a>
          <a href="https://twitter.com/johndoe" target="_blank" rel="noopener noreferrer">Twitter</a>
        </div>
      </div>
      <form @submit.prevent="submitForm" class="contact-form">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="message">Message:</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <button type="submit" :disabled="isSubmitting">{{ isSubmitting ? 'Sending...' : 'Send Message' }}</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactInfo',
  data() {
    return {
      name: '',
      email: '',
      message: '',
      isSubmitting: false
    }
  },
  methods: {
    async submitForm() {
      this.isSubmitting = true
      // Simulate API call
      await new Promise(resolve => setTimeout(resolve, 2000))
      // Here you would typically send the form data to a backend service
      console.log('Form submitted:', { name: this.name, email: this.email, message: this.message })
      // Reset form fields
      this.name = ''
      this.email = ''
      this.message = ''
      this.isSubmitting = false
      alert('Thank you for your message! I will get back to you soon.')
    }
  }
}
</script>

<style scoped>
.contact-info {
  max-width: 800px;
  margin: 0 auto;
}

.contact-content {
  display: flex;
  gap: 40px;
}

.contact-details, .contact-form {
  flex: 1;
}

.contact-details ul {
  list-style-type: none;
  padding: 0;
}

.contact-details li {
  margin-bottom: 10px;
}

.social-links {
  margin-top: 20px;
}

.social-links a {
  margin-right: 15px;
  text-decoration: none;
  color: #007bff;
}

.contact-form {
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input, textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ddd;
  border-radius: 4px;
}

textarea {
  height: 150px;
}

button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #0056b3;
}

button:disabled {
  background-color: #cccccc;
  cursor: not-allowed;
}

@media (max-width: 768px) {
  .contact-content {
    flex-direction