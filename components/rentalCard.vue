<template>
    <div class="rental-grid">
      <div v-for="rental in rentals" :key="rental.id" class="rental-card">
        <div class="rental-image-container">
          <div class="rental-image-background"></div>
            <img class="rental-image" :src="rental.image" alt="rental.title" />
            <h3 class="rental-title">{{ rental.title }}</h3>
        </div>

        <NuxtLink :to="`https://wa.me/${rental.phone}`" target="_blank" class="rental-details">
            إستعلام
        </NuxtLink>
      </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

let rentals = ref([
    {
        image: '/images/rentals/work.png',
        title: 'مكاتب إدارية',
        phone: '0123456789',
    },
    {
        image: '/images/rentals/store.png',
        title: 'محلات',
        phone: '0123456789',   
    },
    {
        image: '/images/rentals/house.png',
        title: ' وحدات سكنية',
        phone: '0123456789',
    }
])
</script>

<style scoped>
.rental-grid{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
    text-align: center;
}

.rental-card{
    background-color: var(--white);
    width: 300px;
    height: 380px;
    border-radius: 30px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
    margin-bottom: 1rem;
    position: relative;
}

.rental-image-container {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 12px;
    width: 300px;
    height: 280px;
    justify-content: center;
    align-items: center;
}

.rental-image-background {
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
.rental-image{
    width: 250px;
    height: 200px;
    top: 12%;
    object-fit:contain ;
    position: relative;
    z-index: 1;
}

.rental-title{
    margin: 2rem 0 0.5rem 0;
    font-size: 1.2rem;
    color: var(--text-color);
}

.rental-details {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: .5rem;
    width: 250px;
    height: 50px;
    background-color: var(--primary-orange);
    border-radius: 50px;
    margin: 1rem auto;
    text-decoration: none;
    color: var(--white);
    font-weight: 600;
    font-size: 1.5rem;
}

</style>