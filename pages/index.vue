<template>
    <main>
      <section class="hero">
        <div class="hero-container">
          <div class="hero-content">
            <div class="hero-main">
  
              
              <div class="hero-text">
                <h1>كل اللي بتحتاجه<br />تحت سقف واحد</h1>
                <div class="hero-buttons">
                  <NuxtLink to="/stores" class="btn btn-outline">المتاجر</NuxtLink>
                  <NuxtLink to="/stores" class="btn btn-primary">الأقسام</NuxtLink>
                </div>
              </div>
              
              
              <div class="logo">
                <img src="@/assets/images/logo.png" alt="مول الصياد بلازا" />
              </div>
            </div>
  
            
            <div class="features">
              <NuxtLink to="/offers" class="feature-item">
                <div class="feature-icon">
                  <img src="@/assets/images/icons/discount.png" alt="عروض" />
                </div>
                <span>عروض</span>
              </NuxtLink>
              <div class="feature-item">
                <div class="feature-icon">
                  <img src="@/assets/images/icons/map.png" alt="خريطة المول" />
                </div>
                <span>خريطة المول</span>
              </div>
              <NuxtLink to="/events" class="feature-item">
                <div class="feature-icon">
                  <img src="@/assets/images/icons/calendar.png" alt="الفاعليات" />
                </div>
                <span>الفاعليات</span>
              </NuxtLink>
              <NuxtLink to="/rentals" class="feature-item">
                <div class="feature-icon">
                  <img src="@/assets/images/icons/lock.png" alt="الايجارات" />
                </div>
                <span>الايجارات</span>
              </NuxtLink>
            </div>
          </div>
        </div>
      </section>
  
       <section class="layers-one">
        
      </section>
      
      <section class="slider-section">
        <AdsSlider />
      </section>
      
      <section class="section-category ">
        <div class="section-header">
          <h2 class="section-title">الأقسام</h2>
          <NuxtLink to="/stores" class="btn-more"><p>المزيد</p></NuxtLink>
        </div>
          <categoryCard />
      </section>
  
      <section class="section-offer">
        <div class="section-header">
          <h2 class="section-title">العروض</h2>
          <NuxtLink to="/offers" class="btn-more"><p>المزيد</p></NuxtLink>
        </div>
          <OffersCard />
      </section>

      <section class="section-stores">
        <div class="section-header">
          <h2 class="section-title">المتاجر</h2>
          <NuxtLink to="/stores" class="btn-more"><p>المزيد</p></NuxtLink>
        </div>
          <storesCard />
      </section>

    </main>
  </template>
  
  <script setup>

  </script>
  
  <style scoped>
  /* Main Container
----------------------------------------*/
main {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
}

/* Hero Section
----------------------------------------*/
.hero {
  background-color: var(--primary-dark);
  width: 100%;
  margin: -3rem auto 0 auto;
  padding: 2rem 0;
  position: relative;
}

.hero-container{
  max-width: 1400px;
  min-height: 600px;
  margin: 0 auto;
  padding: 0 1rem;
}

/* Hero Content
----------------------------------------*/
.hero-content {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: relative;
  padding: 0 1rem;
}

.hero-main {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: -2rem;
  flex-wrap: wrap;
}

/* Hero Text & Buttons */
.hero-text {
  flex: 1;
  text-align: center;
  padding-left: 2rem;
}

.hero-text h1 {
  color: var(--white);
  font-size: 4.2rem;
  font-weight: 700;
  margin-bottom: 2rem;
  line-height: 1.3;
}

.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

/* Logo */
.logo {
  flex: 1;
  text-align: center;
}

.logo img {
  width: 500px;
  height: auto;
  max-width: 100%;
}

/* Features Section
----------------------------------------*/
.features {
  display: flex;
  gap: 3rem;
  justify-content: center;
  /* padding: 0 1rem; */
  margin: 0 auto;
  position: absolute;
  bottom: -180px;
  z-index: 100;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
}

.feature-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  background-color: var(--gray-light);
  border-radius: 40px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  width: 200px;
  height: 200px;
  text-decoration: none;
}

.feature-icon {
  width: 65%;
  height: 65%;
  margin-bottom: 0.5rem;
}

.feature-icon img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.feature-item span {
  color: var(--primary-dark);
  font-weight: 600;
  font-size: 1.5rem;
}

/* Layout Components
----------------------------------------*/


.layers-one {
  background-color: var(--white);
  border-radius: 80px 80px 0 0;
  position: absolute;
  width: 100%;
  max-width: 1400px;
  min-height: 111px;
  margin: -110px auto 0 auto;
  left: 0;
  right: 0;
}

/* Section Components
----------------------------------------*/
.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2rem auto;
  padding: 0 1rem;
  width: 100%;
}

.section-title {
  font-size: 2.4rem;
  font-weight: 700;
  color: var(--primary-dark);
}

/* Sections Styles */
.slider-section {
  margin-top: -6rem;
  margin-bottom: 2rem;
  width: 100%;
}

.section-category {
  background-color: var(--gray-light);
  padding: 0 1rem;
  width: 100%;
  min-height: 450px;
  margin: 4rem auto 1rem auto;
}

.section-offer {
  padding: 0 1rem;
  width: 100%;
  margin: 2rem auto 1rem auto;
}

.section-stores {
  background-color: var(--gray-light);
  padding: 0 1rem;
  width: 100%;
  min-height: 1000px;
  margin: 2rem auto 1rem auto;
}

/* Buttons
----------------------------------------*/
.btn {
  padding: 0.3rem 4rem;
  border-radius: 50px;
  font-size: 1.8rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
}

.btn-primary {
  background-color: var(--primary-orange);
  color: var(--white);
  border: none;
}

.btn-outline {
  background-color: transparent;
  border: 1px solid var(--white);
  color: var(--white);
}

.btn-more {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 180px;
  height: 60px;
  background-color: #f4b52a;
  border-radius: 20px;
  clip-path: path("M0,0 H160 Q140,40 170,80 H0 Z");
  cursor: pointer;
  text-decoration: none;
}

.btn-more p {
  text-align: center;
  color: var(--white);
  font-size: 2.4rem;
  margin-right: 20px;
}

/* Responsive Styles
----------------------------------------*/
/* Screens smaller than 1200px */
@media (max-width: 1200px) {
  .hero-container{
  min-height: 530px;
  margin: 0 auto;
  padding: 0 ;
}
  .hero-text h1 {
    font-size: 3.5rem;
  }
  .btn {
    font-size: 1.6rem;
    padding: 0.3rem 3rem;
  }
  .logo img {
    width: 400px;
  }
  .feature-item {
    width: 170px;
    height: 170px;
  }
  .feature-icon {
    width: 100px;
    height: 100px;
  }
  .feature-item span {
    font-size: 1.3rem;
  }
  .features {
    bottom: -180px;
    gap: 1.7rem;
  }
}

/* Screens smaller than 860px */
@media (max-width: 860px) {
  .hero-container{
  min-height: 480px;
  margin: 0 auto;
  padding: 0 ;
}
  .hero-text h1 {
    font-size: 3rem;
  }
  .btn {
    font-size: 1.4rem;
    padding: 0.2rem 2.5rem;
  }
  .logo img {
    width: 350px;
  }
  .feature-item {
    width: 150px;
    height: 150px;
  }
  .feature-icon {
    width: 85px;
    height: 85px;
  }
  .feature-item span {
    font-size: 1.3rem;
  }
  .features {
    bottom: -180px;
    gap: 1.7rem;
  }
}

/* Tablet and medium screens (less than 768px) */
@media (max-width: 768px) {

  .layers-one{
    border-radius: 40px 40px 0 0;
  }
  .hero-container{
  min-height: 340px;
  margin: 0 auto;
  padding: 0 ;
}
  .hero-main {
    flex-direction: row;
    margin-top: 8px;
  }
  .hero-text {
    padding-left: 0;
  }
  .hero-text h1 {
    font-size: 2rem;
  }
  .btn {
    font-size: 1rem;
    padding: 0.3rem 1.5rem;
  }
  .logo img {
    width: 200px;
  }
  .feature-item {
    width: 110px;
    height: 110px;
    border-radius: 30px;
  }
  .feature-icon {
    width: 55%; 
    height: 55%;
  }
  .feature-item span {
    font-size: 0.8rem;
  }
  .features {
    bottom: -120px;
    gap: .5rem;
    flex-wrap: wrap;
    justify-content: center;
  }
  .section-header {
    padding: 0 2rem;
  }
  .section-title {
  font-size: 2rem;
  font-weight: 700;
  color: var(--primary-dark);
}
  .btn-more {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 140px;
  height: 60px;
  background-color: #f4b52a;
  border-radius: 20px;
  clip-path: path("M0,0 H129.44 Q114.89,31.11 132.22,62.22 H0 Z");
  cursor: pointer;
}

  .btn-more p {
    font-size: 2rem;
  }
}

/* Tablet and medium screens (less than 480px) */
@media (max-width: 480px) {

.hero-container{
min-height: 260px;
margin: 0 auto;
padding: 0 ;
}
.hero-main {
  flex-direction: row;
  margin-top: 8px;
}
.hero-text {
  padding-left: 0;
}
.hero-text h1 {
  font-size: 1.2rem;
}
.btn {
  font-size: .7rem;
    padding: 0.3rem .8rem;
}
.logo img {
  width: 140px;
}
.feature-item {
    width: 75px;
    height: 75px;
    border-radius: 20px;
}
.feature-icon {
    width: 45%; 
    height: 45%;
}
.feature-item span {
  font-size: .5rem;
}
.features {
  bottom: -80px;
  gap: .3rem;
  flex-wrap: wrap;
  justify-content: center;
}
.section-header {
  gap: 1rem;
  align-items: center;
  padding: 0 .5rem;
}
.section-title {
  font-size: 1.8rem;
  font-weight: 700;
  color: var(--primary-dark);
}
.btn-more {
    width: 100px;
    clip-path: path("M0,0 H85.0 Q72.71,29.22 90.22,62.22 H0 Z");
    height: 50px;
    border-radius: 15px; 
}

.btn-more p {
  font-size: 1.3rem;
}
}


/* Small screens (less than 480px) */
/* @media (max-width: 480px) {
  .hero {
    padding: 2rem .1rem;
    margin: -2rem auto 0 auto;
  }
  .hero-text h1 {
    font-size: 1.2rem;
  }
  .btn {
    font-size: .7rem;
    padding: 0.3rem .8rem;
  }
  .logo img {
    width: 250px;
  }
  .feature-item {
    width: 75px;
    height: 75px;
    border-radius: 20px;
  }
  .feature-icon {
    width: 45%; 
    height: 45%;
  }
  .feature-item span {
    font-size: .5rem;

  }
  .features {
    bottom: -150px;
    gap: .3rem;
  }

  .section-title {
  font-size: 1.8rem;
  font-weight: 700;
  color: var(--primary-dark);
}
  .section-header {
    gap: 1rem;
    align-items: flex-center;
    padding: 0 1rem;
  }

  .btn-more {
    width: 100px;
    clip-path: path("M0,0 H85.0 Q72.71,29.22 90.22,62.22 H0 Z");
    height: 50px;
    border-radius: 15px;
  }
  .btn-more p {
    font-size: 1.5rem;
  }
} */

</style>