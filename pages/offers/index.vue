<template>
    <main>
        <section class="slider-section">
            <AdsSlider />
        </section>
        <div class="title">العروض</div>

        <section class="section-offer">
            <OffersCard />
        </section>
        <section class="section-offer">
            <OffersCard />
        </section>
    </main>
    
</template>

<script setup>

</script>

<style scoped>

main {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
}



.slider-section {
  margin-top: -6rem;
  margin-bottom: 2rem;
  width: 100%;
  
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
.section-offer {
  padding: 0 1rem;
  width: 100%;
  margin: 1rem auto 1rem auto;
}
</style>