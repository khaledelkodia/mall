<script setup>
  
</script>

<template>
  <header class="main-header">
    <div class="header-content">
      <div class="logo">
        <img src="@/assets/images/logo.png" alt="مول الصياد بلازا" />
      </div>
      <div class="nav-container">
        <nav class="main-nav">
          <ul>
            <li><NuxtLink to="/offers">عروض</NuxtLink></li>
            <li><NuxtLink to="/maps">خريطة المول</NuxtLink></li>
            <li><NuxtLink to="/events">فاعليات</NuxtLink></li>
            <li><NuxtLink to="/rentals">الإيجارات</NuxtLink></li>
          </ul>
        </nav>
        <nav class="main-nav">
          <ul>
            <li><NuxtLink to="/about">معلومات عنا</NuxtLink></li>
            <li><NuxtLink to="/hours">ساعات العمل</NuxtLink></li>
            <li><NuxtLink to="/contact">عنوانا</NuxtLink></li>
          </ul>
        </nav>
        <nav class="main-nav">
          <ul>
            <li><NuxtLink to="/stores">الأقسام</NuxtLink></li>
            <li><NuxtLink to="/stores">المتاجر</NuxtLink></li>
            <li><NuxtLink to="/products">المنتجات</NuxtLink></li>
          </ul>
        </nav>
      </div>
      <div class="social-media">
        <h1>السوشيال ميديا</h1>
        <div class="social-icons">
          <a href="https://facebook.com">
            <img src="/images/icons/facebook.png" alt="Facebook" />
          </a>
          <a href="https://instagram.com">
            <img src="/images/icons/instagram.png" alt="Instagram" />
          </a>
          <a href="https://tiktok.com">
            <img src="/images/icons/tiktok.png" alt="Tiktok" />
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>

.main-header {
  background-color: var(--primary-dark);
  padding: 0 0 2rem 2rem;
  border-top-left-radius: 50px;
  border-top-right-radius: 50px;
  width: 100%;
  max-width: 1400px;
  height: 330px;
  margin: 0 auto;
  z-index: 100;
}

.header-content {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
}

.logo {
  width: 320px;
  height: 320px;
}
.logo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.nav-container {
  display: flex;
  gap: 8rem;
  justify-content: space-around;
}
.main-nav ul {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  list-style: none;
  padding: 0;
  margin: 0;
}
.main-nav a {
  color: var(--white);
  text-decoration: none;
  font-size: 1rem; 
  transition: color 0.3s ease;
  font-weight: 500;
}
.main-nav a:hover {
  color: var(--primary-orange);
}

.social-media {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1.5rem;
}
.social-media h1 {
    color: var(--primary-orange);
  font-size: 1.2rem; 
}
.social-icons a img {
  width: 80px; 
}




@media (max-width: 1200px) {

 .main-header {
    height: 250px;
  }
  .nav-container {
    gap: 4rem;
  }
  .logo {
  width: 250px;
  height: 250px;
}
.logo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.social-icons a img {
    width: 60px;
  }
}

@media (max-width: 900px) {

  .main-header {
    height: 250px;
  }

  .nav-container {
    gap: 1.8rem;
  }
  .social-icons a img {
    width: 40px;
  }
  .social-media h1 {
  
  font-size: 1rem; 
}
}


@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  .logo {
    width: 300px;
    height: 300px;
  }
  .nav-container {
    flex-direction: column;
    gap: 1.5rem;
    align-items: center;
    text-align: center;
  }
  .main-header {
    height: auto;
    padding: 2rem 1rem;
  }
  .main-nav a {
    font-size: 1.5rem;
  }
  .social-media h1 {
    color: var(--primary-orange);
    font-size: 1.6rem;
  }
  .social-icons a img {
    width: 60px;
  }
}


@media (max-width: 480px) {
    .main-header {
        border-top-left-radius: 30px;
  border-top-right-radius: 30px;
      }
  .main-nav a {
    font-size: 0.9rem;
  }
  .social-media h1 {
    font-size: 0.9rem;
  }
  .social-icons a img {
    width: 50px;
  }
  .logo {
    width: 250px;
    height: 250px;
  }
}
</style>
