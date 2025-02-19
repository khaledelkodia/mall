<template>
    <div class="schedule-container">
      <p class="countdown"> <span v-if="closeAfter">الإغلاق بعد :   {{ hours }}</span> {{ remainingTime }} </p>
  
      <div class="schedule-table">
        <table>
          <thead>
            <tr>
              <th>اليوم</th>
              <th>من</th>
              <th>إلى</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="time in schedule" :key="time.day" :class="{ today: time.day === currentDay }">
              <td class="day">{{ time.day }}</td>
              <td class="time">{{ time.from }}</td>
              <td class="time">{{ time.to }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, computed, onMounted, onUnmounted } from "vue";
  
  const schedule = ref([
    { day: "السبت", from: "10:00 ص", to: "11:00 م" },
    { day: "الأحد", from: "10:00 ص", to: "11:00 م" },
    { day: "الإثنين", from: "10:00 ص", to: "11:00 م" },
    { day: "الثلاثاء", from: "10:00 ص", to: "11:00 م" },
    { day: "الأربعاء", from: "10:00 ص", to: "11:00 م" },
    { day: "الخميس", from: "10:00 ص", to: "12:00 ص" },
    { day: "الجمعة", from: "4:00 م", to: "12:00 ص" }
  ]);
  
  const closeAfter = ref(true);
  const daysMap = ["الأحد", "الإثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة", "السبت"];
  const currentDay = ref(daysMap[new Date().getDay()]);
  
  const remainingTime = ref("");
  let timer = null;
  
  const updateRemainingTime = () => {
  const now = new Date();
  const todaySchedule = schedule.value.find((s) => s.day === currentDay.value);

  if (!todaySchedule) {
    remainingTime.value = "غير متاح";
    return;
  }

  let [hours, minutes] = todaySchedule.to.match(/\d+/g).map(Number);
  if (todaySchedule.to.includes("م") && hours !== 12) hours += 12;
  if (todaySchedule.to.includes("ص") && hours === 12) hours = 0;

  const closingTime = new Date();
  closingTime.setHours(hours, minutes, 0, 0);

  if (hours === 0) {
    closingTime.setDate(closingTime.getDate() + 1);
  }

  const diffMs = closingTime - now;
  if (diffMs <= 0) {
    closeAfter.value = false;
    remainingTime.value = "المول مغلق الآن";
    return;
  }

  const hoursLeft = Math.floor(diffMs / (1000 * 60 * 60));
  const minutesLeft = Math.floor((diffMs % (1000 * 60 * 60)) / (1000 * 60));
  const secondsLeft = Math.floor((diffMs % (1000 * 60)) / 1000);

  remainingTime.value = `${hoursLeft} ساعة و ${minutesLeft} دقيقة و ${secondsLeft} ثانية`;
};

  onMounted(() => {
    updateRemainingTime();
    timer = setInterval(updateRemainingTime, 1000);
  });
  
  onUnmounted(() => {
    clearInterval(timer);
  });
  </script>
  
  <style scoped>
  .schedule-container {
    text-align: center;
    padding: 20px;
  }
  
  
  
  .countdown {
    font-size: 25px;
    font-weight: bold;
    color: var(--primary-dark);
    margin-bottom: 15px;
  }
  
  .schedule-table {
    max-width: 1400px;
    margin: auto;
    padding: 20px;
  }
  
  table {
    width: 100%;
    border-collapse: collapse;
    background: var(--white);
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
  }
  
  th, td {
    padding: 15px 18px;
    text-align: center;
    font-size: 22px;
  }
  
  th {
    background: var(--primary-dark);
    color: var(--white);
    font-weight: bold;
  }
  
  td {
    border-bottom: 8px double var(--gray-light);
  }
  
  .today {
    background: var(--primary-orange);
    font-weight: bold;
    color: white;
  }
  
  tbody tr:hover {
    background: #ffcc80;
  }
  
  @media (max-width: 480px) {
    th, td {
      padding: 10px;
      font-size: 14px;
    }
  }
  </style>
  