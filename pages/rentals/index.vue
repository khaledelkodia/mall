<template>
    <main>
        <div class="title"> الإيجارات</div>
        <section class="section-rentals">
            <rentalCard />
        </section>
        
    </main>
    
</template>

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

.section-rentals{ 
    padding: 2rem 1rem;
    width: 100%;
    margin: 3rem auto 1rem auto;
 }

</style>