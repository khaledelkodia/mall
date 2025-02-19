<script setup>

</script>

<template>
  <header class="main-header">
    <div class="header-content">
      <nav class="main-nav">
        <ul>
          <li><NuxtLink to="/">الرئيسية</NuxtLink></li>
          <li><NuxtLink to="/about">معلومات عنا</NuxtLink></li>
          <li><NuxtLink to="/hours">ساعات العمل</NuxtLink></li>
        </ul>
      </nav>

      <div class="search-box">
        <button type="button" class="search-btn">
          <i class="fas fa-search"></i>
        </button>
        <input type="text" placeholder="ابحث عن متجر..." />
      </div>
    </div>
  </header>
</template>

<style scoped>
/* الأساسيات */
.main-header {
  background-color: var(--primary-dark);
  padding: 2rem;
  border-bottom-left-radius: 50px;
  border-bottom-right-radius: 50px;
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  z-index: 100;
}

.header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.search-box {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  background: var(--white);
  border-radius: 50px;
  padding: 0.6rem 1.2rem;
  margin-left: 2rem;
  width: 600px;
}

.search-box input {
  border: none;
  background: none;
  width: 100%;
  padding: 0.25rem;
  font-size: 0.9rem;
  font-family: 'Tajawal', sans-serif;
}

.search-box input::placeholder {
  color: #999;
  font-family: 'Tajawal', sans-serif;
  font-weight: 400;
}

.search-box input:focus {
  outline: none;
}

.search-btn {
  background: none;
  border: none;
  color: var(--primary-orange);
  cursor: pointer;
  padding: 0.25rem 0.5rem 0.25rem 0;
  font-size: 1rem;
}

.main-nav ul {
  display: flex;
  gap: 2.5rem;
  list-style: none;
  margin: 0;
  margin-right: 2rem;
  padding: 0;
}

.main-nav a {
  color: var(--white);
  text-decoration: none;
  font-size: 1.5rem;
  transition: color 0.3s ease;
  padding: 0.5rem 0;
  font-weight: 500;
}

.main-nav a:hover {
  color: var(--primary-orange);
}

/* التحسينات للعرض على شاشات مختلفة */

/* شاشات متوسطة وأقل من 1200px */
@media (max-width: 1200px) {
  .main-header {
    padding: 1.5rem;
  }
  .main-nav ul {
    gap: 2rem;
  }
  .search-box {
    width: 40%;
    margin-left: 1rem;
  }
}

/* شاشات التابلت والهواتف (أقل من 768px) */
@media (max-width: 860px) {
  .header-content {
    flex-direction: column;
    align-items: stretch;
    gap: 1rem;
  }
  .main-nav ul {
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    gap: 1rem;
    margin-right: 0;
  }
  .search-box {
    width: 100%;
    margin: 0;
  }
}

/* شاشات الهواتف الصغيرة (أقل من 480px) */
@media (max-width: 480px) {
  .main-header{
    border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
  }
  .main-nav a {
    font-size: 0.9rem;
  }
  .search-box input {
    font-size: 0.8rem;
  }
  .search-btn {
    font-size: 0.8rem;
  }
}

@media (max-width: 365px) {
  .main-nav a {
    font-size: .9rem;
  }
  .search-box input {
    font-size: 0.8rem;
  }
  .search-btn {
    font-size: 0.8rem;
  }
}
</style>

