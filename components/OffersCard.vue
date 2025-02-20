<template>
  <div class="offers-grid">
    <div v-for="offer in offers" :key="offer.id" class="offer-card">
    <div class="isOffer">عرض</div>
    <div class="offer-image">
      <img :src="offer.image" :alt="offer.title" />
    </div>
    <div class="offer-details">
      <h3 class="offer-title">{{ offer.title }}</h3>
      <h3 class="offer-store">{{ offer.store }}</h3>
      <div class="offer-meta">
        <div class="price-container">
          <div class="price">{{ offer.price }}</div>
          <div class="currency">جنية</div>  
        </div>
        <hr class="vertical-line">
        <div class="views">
          <img class="icon-views" src="/images/icons/view.png" alt="">
          <span class="view-product">مشاهدة المنتج</span>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script setup>
defineOptions({
  name: 'OffersCard'
})

const offers = [
  {
    id: 1,
    title: 'ساعة رياضية سمارت',
    price: 2500,
    views: 2300,
    image: '/images/products/watch.png',
    store: "مكتبتي"
  },
  {
    id: 2,
    title: 'قميص اسود',
    price: 350,
    views: 1500,
    image: '/images/products/shirt.png',
    store: "مكتبتي"
  },
  {
    id: 3,
    title: 'مكنسة كهربائية',
    price: 2700,
    views: 800,
    image: '/images/products/vacuum.png',
    store: "مكتبتي"
  },
  {
    id: 4,
    title: 'جاكيت شتوي',
    price: 750,
    views: 1200,
    image: '/images/products/jacket.png',
    store: "مكتبتي"
  },
  {
    id: 1,
    title: 'ساعة رياضية سمارت',
    price: 2500,
    views: 2300,
    image: '/images/products/watch.png',
    store: "مكتبتي"
  },
  {
    id: 2,
    title: 'قميص اسود',
    price: 350,
    views: 1500,
    image: '/images/products/shirt.png',
    store: "مكتبتي"
  },
  {
    id: 3,
    title: 'مكنسة كهربائية',
    price: 2700,
    views: 800,
    image: '/images/products/vacuum.png',
    store: "ملابسي"
  },
  {
    id: 4,
    title: 'جاكيت شتوي',
    price: 750,
    views: 1200,
    image: '/images/products/jacket.png',
    store: "موبايلي"
  }
]
</script>

<style scoped>
  .offers-grid {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
    text-align: center;
  }

.offer-card {
  background-color: var(--gray-light);
  width: 300px;
  height: 380px;
  border-radius: 30px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
  margin-bottom: 1rem;
  position: relative;
}

.isOffer {
  position: absolute;
  top: 18px;
  right: 20px;
  width: 70px;
  background-color: var(--primary-orange);
  color: var(--white);
  font-weight: 600;
  border-radius: 50px;
}


.offer-image{
  background-color: var(--white);
  width: 280px;
  height: 200px;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  margin-top: 15px;
  margin-left: auto;
  margin-right: auto;
}

.offer-image img {
  width: 210px;
  object-fit: cover;
}

.offer-details {
  padding: 1rem;
}

.offer-title {
  margin: 0 0 0.5rem 0;
  font-size: 1.2rem;
  color: var(--text-color);
}

.offer-store {
  margin: 0 0 0.5rem 0;
  font-size: 1rem;
  color: #1183C7;
}

.offer-meta {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.price-container{
  display: flex;
  flex-direction: column;
  align-items: center;
}

.price {
  color: var(--primary-dark);
  font-weight: bold;
  font-size: 1.6rem;
}

.currency{
  color: var(--primary-dark);
  font-size: 1rem;
  font-weight: bold;
}

.vertical-line {
  position: absolute;
  height: 70px; 
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 1px; 
  background-color: var(--primary-dark); 
}

.views {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.icon-views {
  width: 45px;
  height: 45px;
}

.view-product {
  color: var(--primary-dark);
  font-weight: bold;
  font-size: 0.7rem;
}
</style>
