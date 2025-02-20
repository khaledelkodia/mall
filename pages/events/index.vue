<template>
  <main>
  <div class="events-page">
    <div class="container">
      <h1 class="title">الفعاليات</h1>
      <section class="events-grid">
        <EventCard
          v-for="event in events"
          :key="event.id"
          :image="event.image"
          :title="event.title"
          :day="event.day"
          :month="event.month"
          :time="event.time"
          :duration="event.duration"
        />
      </section>
    </div>
  </div>
</main>
</template>

<script setup>
import { ref } from 'vue';

const events = ref([
        {
          id: 1,
          image: '/images/events/gaming.webp',
          title: 'تحدي أجمد واحد في البلايستيشن',
          day: '23',
          month: 'مايو',
          time: '3:00 م',
          duration: 'لمدة 3 أيام'
        },
        {
          id: 2,
          image: '/images/events/ramadan.jpg',
          title: 'خيمة رمضان فطار وسحور',
          day: '28',
          month: 'فبراير',
          time: '4:30 م',
          duration: 'لمدة 30 يوم'
        },
        {
          id: 3,
          image: '/images/events/games.jpg',
          title: 'تخفيضات علي الملاهي',
          day: '1',
          month: 'مارس',
          time: '12:00 م',
          duration: 'لمدة 10 أيام'
        },
        {
          id: 3,
          image: '/images/events/games.jpg',
          title: 'تخفيضات علي الملاهي',
          day: '1',
          month: 'مارس',
          time: '12:00 م',
          duration: 'لمدة 10 أيام'
        },
      ])
    
</script>

<style scoped>
main {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
}

.title{
  font-size: 2rem;
  font-weight: 900;
  color: var(--primary-dark);
  margin-bottom: 2rem;
  margin-top: 2rem;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title::after {
  content: "";
  width: 30%;
  height: 1px;
  background-color: var(--primary-orange);
  margin: 3rem 2rem;
}

.title::before {
  content: "";
  width: 30%;
  height: 1px;
  background-color: var(--primary-orange);
  margin: 3rem 2rem;
}


.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px 20px;
}

.events-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  padding: 2px 0;
}

@media (max-width: 768px) {
  .events-page {
    padding: 20px 0;
  }

  .events-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}
</style>
