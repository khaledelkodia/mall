<template>
    <div class="categories-grid">
        <div v-for="category in categories" :key="category.id">
            <div class="category-item">
                <img :src="category.image" :alt="category.title" />
            </div>
            <span class="category-title">{{ category.title }}</span>
        </div>
    </div>
</template>

<script setup>
const categories = [
{ id: 1, title: 'الأزياء والموضة', image: '/images/categories/clothes.png' },
{ id: 2, title: 'الإلكترونيات', image: '/images/categories/electronics.png' },
{ id: 3, title: 'الجمال والعناية', image: '/images/categories/entertainment.png' },
{ id: 4, title: 'الأطفال', image: '/images/categories/fashion.png' },
{ id: 5, title: 'الطعام', image: '/images/categories/food.png' },
{ id: 6, title: 'مجوهرات وساعات', image: '/images/categories/watches.png' },
]
</script>

<style scoped>
.categories-grid {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 1rem;
  text-align: center;
}

.category-item {
  background-color: var(--white);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  width: 200px;
  height: 200px;
  border-radius: 40px;
  cursor: pointer;
  position: relative;
  margin-bottom: 1rem;
}

.category-item img {
  width: 250px;
  height: 250px;
  object-fit: cover;
  position: absolute;
  top: -40px;
  left: 50%;
  transform: translateX(-50%);
}

.category-title {
  color: var(--primary-dark);
  font-weight: 700;
  font-size: 1.2rem;
}

</style>