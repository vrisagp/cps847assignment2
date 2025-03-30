<template>
  <div class="home">
    <div class="hero">
      <div class="hero-content">
        <h1>Welcome to MyCompany Inc.</h1>
        <p>Your trusted partner in IT consulting and digital transformation</p>
      </div>
    </div>
    
    <div class="info-container">
      <div class="info-card datetime">
        <div class="icon">🕒</div>
        <h2>Current Date and Time</h2>
        <p class="time">{{ formattedDateTime }}</p>
      </div>
      
      <div class="info-card weather">
        <div class="icon">🌡️</div>
        <h2>Belleville Temperature</h2>
        <p v-if="temperature" class="temperature">{{ temperature }}°C</p>
        <p v-else class="loading">Loading temperature...</p>
      </div>
    </div>

    <div class="features">
      <div class="feature-card">
        <div class="icon">💡</div>
        <h3>Innovation</h3>
        <p>Cutting-edge solutions for modern businesses</p>
      </div>
      <div class="feature-card">
        <div class="icon">🤝</div>
        <h3>Partnership</h3>
        <p>Working together to achieve your goals</p>
      </div>
      <div class="feature-card">
        <div class="icon">⚡</div>
        <h3>Efficiency</h3>
        <p>Streamlined processes for better results</p>
      </div>
    </div>
  </div>
</template>

<script>
import { format } from 'date-fns'

export default {
  name: 'Home',
  data() {
    return {
      formattedDateTime: format(new Date(), 'yyyy-MM-dd HH:mm:ss'),
      temperature: null
    }
  },
  async created() {
    try {
      const response = await fetch(
        'https://api.openweathermap.org/data/2.5/weather?q=Belleville,CA&appid=af3ee10a3cccdbf8c52faa0a689bd014&units=metric'
      )
      const data = await response.json()
      this.temperature = Math.round(data.main.temp)
    } catch (error) {
      console.error('Error fetching weather data:', error)
    }
  }
}
</script>

<style scoped>
.home {
  min-height: 100vh;
}

.hero {
  background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
  color: white;
  padding: 6rem 2rem;
  text-align: center;
  margin-bottom: 3rem;
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.hero p {
  font-size: 1.2rem;
  opacity: 0.9;
}

.info-container {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-bottom: 4rem;
  flex-wrap: wrap;
  padding: 0 2rem;
}

.info-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  min-width: 300px;
  transition: transform 0.3s ease;
}

.info-card:hover {
  transform: translateY(-5px);
}

.icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.info-card h2 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.time, .temperature {
  font-size: 2rem;
  color: #42b983;
  font-weight: 600;
}

.loading {
  color: #666;
  font-style: italic;
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  padding: 2rem;
  background-color: #f8f9fa;
}

.feature-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-card h3 {
  color: #2c3e50;
  margin: 1rem 0;
}

.feature-card p {
  color: #666;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .hero {
    padding: 4rem 1rem;
  }

  .hero h1 {
    font-size: 2rem;
  }

  .info-container {
    padding: 0 1rem;
  }

  .features {
    padding: 1rem;
  }
}
</style> 