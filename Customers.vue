<template>
  <div class="customers">
    <div class="customers-hero">
      <h1>Our Customers</h1>
      <p>Trusted by Industry Leaders</p>
    </div>

    <div class="customers-content">
      <div class="customer-card">
        <div class="customer-icon">🏢</div>
        <h3>TechCorp</h3>
        <p class="industry">Technology Solutions</p>
        <p class="testimonial">"MyCompany Inc. transformed our IT infrastructure and helped us achieve significant cost savings while improving efficiency."</p>
        <div class="customer-details">
          <p>Location: Toronto, ON</p>
          <p>Project: Digital Transformation</p>
        </div>
      </div>

      <div class="customer-card">
        <div class="customer-icon">💼</div>
        <h3>FinancePro</h3>
        <p class="industry">Financial Services</p>
        <p class="testimonial">"The team at MyCompany Inc. provided exceptional consulting services that helped us modernize our financial systems."</p>
        <div class="customer-details">
          <p>Location: Toronto, ON</p>
          <p>Project: System Modernization</p>
        </div>
      </div>

      <div class="customer-card">
        <div class="customer-icon">🏥</div>
        <h3>HealthCare Plus</h3>
        <p class="industry">Healthcare Solutions</p>
        <p class="testimonial">"Their expertise in healthcare IT solutions helped us improve patient care and streamline our operations."</p>
        <div class="customer-details">
          <p>Location: Toronto, ON</p>
          <p>Project: Healthcare IT Integration</p>
        </div>
      </div>

      <div class="customer-card">
        <div class="customer-icon">🏭</div>
        <h3>ManufacturePro</h3>
        <p class="industry">Manufacturing</p>
        <p class="testimonial">"The automation solutions provided by MyCompany Inc. significantly improved our production efficiency."</p>
        <div class="customer-details">
          <p>Location: Toronto, ON</p>
          <p>Project: Process Automation</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.customers {
  min-height: 100vh;
}

.customers-hero {
  background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
  margin-bottom: 3rem;
}

.customers-hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.customers-hero p {
  font-size: 1.2rem;
  opacity: 0.9;
}

.customers-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.customer-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
}

.customer-card:hover {
  transform: translateY(-5px);
}

.customer-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
  text-align: center;
}

.customer-card h3 {
  color: #2c3e50;
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  text-align: center;
}

.industry {
  color: #42b983;
  font-weight: 500;
  text-align: center;
  margin-bottom: 1rem;
}

.testimonial {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  font-style: italic;
  flex-grow: 1;
}

.customer-details {
  border-top: 1px solid #eee;
  padding-top: 1rem;
}

.customer-details p {
  color: #666;
  margin: 0.5rem 0;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .customers-hero {
    padding: 3rem 1rem;
  }

  .customers-hero h1 {
    font-size: 2rem;
  }

  .customers-content {
    padding: 0 1rem;
  }
}
</style> 