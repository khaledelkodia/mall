<template>
  <div class="event-card">
    <div class="event-image-container">
      <img :src="image" :alt="title" class="event-image" />
      <div class="event-date">
        <span class="day">{{ day }}</span>
        <span class="month">{{ month }}</span>
      </div>
    </div>
    <div class="event-details">
      <h3 class="event-title">{{ title }}</h3>
      <div class="event-info">
        <div class="time-info">
          <i class="fas fa-clock"></i>
          <span>{{ time }}</span>
        </div>
        <div class="duration-info">
          <i class="fas fa-calendar-alt"></i>
          <span>{{ duration }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    day: {
      type: String,
      required: true
    },
    month: {
      type: String,
      required: true
    },
    time: {
      type: String,
      required: true
    },
    duration: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.event-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  width: 100%;
  margin-bottom: 20px;
}

.event-card:hover {
  transform: translateY(-5px);
}

.event-image-container {
  position: relative;
  width: 100%;
  padding-top: 60%; /* Aspect ratio 16:9 */
  overflow: hidden;
}

.event-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.event-date {
  position: absolute;
  top: 15px;
  right: 15px;
  background: var(--primary-orange);
  padding: 10px;
  border-radius: 8px;
  text-align: center;
  min-width: 60px;
}

.day {
  display: block;
  font-size: 1.5rem;
  font-weight: bold;
  color: var(--white);
}

.month {
  display: block;
  font-size: 0.9rem;
  color: var(--white);
}

.event-details {
  padding: 20px;
}

.event-title {
  margin: 0 0 15px 0;
  font-size: 1.2rem;
  color:var(--primary-dark);
  font-weight: 600;
}

.event-info {
  display: flex;
  gap: 20px;
  color: var(--primary-dark);
  font-size: 0.9rem;
}

.time-info, .duration-info {
  display: flex;
  align-items: center;
  gap: 8px;
}

.fas {
  color: var(--primary-orange);
}

@media (max-width: 768px) {
  .event-card {
    margin-bottom: 15px;
  }

  .event-title {
    font-size: 1.1rem;
  }

  .event-info {
    flex-direction: column;
    gap: 10px;
  }
}
</style>
