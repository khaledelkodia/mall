<template>
  <div class="offers-grid">
    <div v-for="offer in offers" :key="offer.id" class="offer-card">
    <div v-if="offer.isOffer" class="isOffer">عرض</div>
    <div class="offer-image-container">
        <div class="offer-image-background"></div>
        <img class="offer-image" :src="offer.image" :alt="offer.title" />
      <h3 class="offer-title">{{ offer.title }}</h3>
    </div>
    
    <div class="offer-details">
     
      <div class="offer-meta">
        <div class="views">
          <img class="icon-views" src="/images/icons/view.png" alt="">
          <span class="view-product">مشاهدة المنتجات</span>
        </div>
        <hr class="vertical-line">
        <div class="views">
          <img class="icon-views" src="/images/icons/pin.png" alt="">
          <span class="view-product"> مكان المتجر</span>
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
    title: 'سيدار',
    image: '/images/stores/sedar.png',
    isOffer: true
  },
  {
    id: 2,
    title: ' نباتاتي',
    image: '/images/stores/nabataty.png',
    isOffer: true
  },
  {
    id: 3,
    title: ' كاردا',
    image: '/images/stores/Carda.png',
    isOffer: false
  },
  {
    id: 4,
    title: ' أمريكان إيجلز',
    image: '/images/stores/american eagle.png',
    isOffer: true
  },
  {
    id: 5,
    title: 'فوغا كلوسيت',
    image: '/images/stores/VogaCloset.png',
    isOffer: false
  },
  {
    id: 6,
    title: ' نيو بلانس',
    image: '/images/stores/new balance.png',
    isOffer: true
  },
  {
    id: 7,
    title: ' بات بات',
    image: '/images/stores/patpat.svg',
    isOffer: false
  },
  {
    id: 8,
    title: ' رسيس',
    image: '/images/stores/rasess.svg',
    isOffer: true
  },
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
  background-color: var(--white);
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


.offer-image-container {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 12px;
    width: 300px;
    height: 280px;
    justify-content: center;
    align-items: center;
}

.offer-image-background {
    position: absolute;
    top: 56%;
    left: 50%;
    width: 220px;
    height: 200px;
    background-color: #6B6BE9;
    opacity: 0.34;
    filter: blur(20px);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    z-index: 0;
}

.offer-image {
    width: 250px;
    height: 200px;
    top: 12%;
    object-fit:contain ;
    position: relative;
    z-index: 1;
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

