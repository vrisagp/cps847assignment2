<template>
  <div class="about">
    <div class="about-hero">
      <h1>About Us</h1>
      <p>Your Trusted Partner in IT Consulting</p>
    </div>

    <div class="about-content">
      <div class="about-section">
        <div class="section-content">
          <h2>Our Story</h2>
          <p>MyCompany Inc. is a leading IT consulting company based in downtown Toronto. We specialize in delivering innovative technology solutions to businesses across various industries.</p>
          <p>With years of experience and a team of expert professionals, we help our clients navigate the digital landscape and achieve their business objectives.</p>
        </div>
        <div class="section-image">
          <div class="image-placeholder">🏢</div>
        </div>
      </div>

      <div class="about-section reverse">
        <div class="section-content">
          <h2>Our Mission</h2>
          <p>To empower businesses with cutting-edge technology solutions that drive growth, efficiency, and innovation.</p>
          <p>We believe in building long-term partnerships with our clients, understanding their unique needs, and delivering tailored solutions that make a real difference.</p>
        </div>
        <div class="section-image">
          <div class="image-placeholder">🎯</div>
        </div>
      </div>

      <div class="about-section">
        <div class="section-content">
          <h2>Our Values</h2>
          <ul class="values-list">
            <li>Innovation and Creativity</li>
            <li>Client Success</li>
            <li>Integrity and Trust</li>
            <li>Continuous Learning</li>
            <li>Team Collaboration</li>
          </ul>
        </div>
        <div class="section-image">
          <div class="image-placeholder">💎</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about {
  min-height: 100vh;
}

.about-hero {
  background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
  margin-bottom: 3rem;
}

.about-hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.about-hero p {
  font-size: 1.2rem;
  opacity: 0.9;
}

.about-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.about-section {
  display: flex;
  align-items: center;
  gap: 4rem;
  margin-bottom: 4rem;
  padding: 2rem;
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.about-section.reverse {
  flex-direction: row-reverse;
}

.section-content {
  flex: 1;
}

.section-content h2 {
  color: #2c3e50;
  font-size: 2rem;
  margin-bottom: 1.5rem;
}

.section-content p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.section-image {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-placeholder {
  font-size: 4rem;
  padding: 2rem;
  background: #f8f9fa;
  border-radius: 12px;
  min-width: 200px;
  text-align: center;
}

.values-list {
  list-style: none;
  padding: 0;
}

.values-list li {
  color: #666;
  line-height: 1.6;
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
  position: relative;
}

.values-list li::before {
  content: "•";
  color: #42b983;
  position: absolute;
  left: 0;
}

@media (max-width: 768px) {
  .about-hero {
    padding: 3rem 1rem;
  }

  .about-hero h1 {
    font-size: 2rem;
  }

  .about-section {
    flex-direction: column;
    gap: 2rem;
    padding: 1.5rem;
  }

  .about-section.reverse {
    flex-direction: column;
  }

  .section-image {
    order: -1;
  }
}
</style> 