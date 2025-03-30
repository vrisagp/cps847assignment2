<template>
  <div class="services">
    <div class="services-hero">
      <h1>Our Services</h1>
      <p>Comprehensive IT Solutions for Your Business</p>
    </div>

    <div class="services-content">
      <div class="service-card">
        <div class="service-icon">💻</div>
        <h3>IT Consulting</h3>
        <p>Strategic technology consulting to help businesses make informed decisions. We analyze your current IT infrastructure and provide recommendations for improvement.</p>
        <ul class="service-features">
          <li>Technology Assessment</li>
          <li>Strategic Planning</li>
          <li>Risk Management</li>
        </ul>
      </div>

      <div class="service-card">
        <div class="service-icon">⚙️</div>
        <h3>Software Development</h3>
        <p>Custom software solutions tailored to your business needs. We develop scalable and maintainable applications that drive your business forward.</p>
        <ul class="service-features">
          <li>Custom Applications</li>
          <li>Web Development</li>
          <li>Mobile Apps</li>
        </ul>
      </div>

      <div class="service-card">
        <div class="service-icon">🔄</div>
        <h3>Digital Transformation</h3>
        <p>Help your business evolve in the digital age with modern solutions. We guide you through the process of digital transformation.</p>
        <ul class="service-features">
          <li>Process Automation</li>
          <li>Cloud Migration</li>
          <li>Digital Strategy</li>
        </ul>
      </div>

      <div class="service-card">
        <div class="service-icon">🛡️</div>
        <h3>Cybersecurity</h3>
        <p>Protect your business with comprehensive security solutions. We help you identify and mitigate security risks.</p>
        <ul class="service-features">
          <li>Security Assessment</li>
          <li>Threat Protection</li>
          <li>Compliance</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.services {
  min-height: 100vh;
}

.services-hero {
  background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
  margin-bottom: 3rem;
}

.services-hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.services-hero p {
  font-size: 1.2rem;
  opacity: 0.9;
}

.services-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.service-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
}

.service-card:hover {
  transform: translateY(-5px);
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
  text-align: center;
}

.service-card h3 {
  color: #2c3e50;
  font-size: 1.5rem;
  margin-bottom: 1rem;
  text-align: center;
}

.service-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  flex-grow: 1;
}

.service-features {
  list-style: none;
  padding: 0;
  margin: 0;
}

.service-features li {
  color: #666;
  line-height: 1.6;
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
  position: relative;
}

.service-features li::before {
  content: "✓";
  color: #42b983;
  position: absolute;
  left: 0;
}

@media (max-width: 768px) {
  .services-hero {
    padding: 3rem 1rem;
  }

  .services-hero h1 {
    font-size: 2rem;
  }

  .services-content {
    padding: 0 1rem;
  }
}
</style> 