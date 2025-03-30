<template>
  <div class="app">
    <nav class="navbar">
      <div class="logo">
        <h1>MyCompany Inc.</h1>
      </div>
      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About Us</router-link>
        <router-link to="/services">Our Services</router-link>
        <router-link to="/customers">Our Customers</router-link>
      </div>
    </nav>
    <router-view></router-view>
    <footer class="footer">
      <p>&copy; 2024 MyCompany Inc. All rights reserved.</p>
    </footer>
  </div>
</template>

<style>
.app {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.navbar {
  background-color: #ffffff;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo h1 {
  color: #2c3e50;
  margin: 0;
  font-size: 1.5rem;
  font-weight: 600;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  color: #2c3e50;
  text-decoration: none;
  font-weight: 500;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  transition: all 0.3s ease;
}

.nav-links a:hover {
  background-color: #f8f9fa;
  color: #42b983;
}

.nav-links a.router-link-active {
  color: #42b983;
  font-weight: 600;
}

.footer {
  background-color: #2c3e50;
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: auto;
}

@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    padding: 1rem;
  }

  .nav-links {
    margin-top: 1rem;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
  }
}
</style> 