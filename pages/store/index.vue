<template>
    <main>

        <div class="store-container">
            <div class="store-name">
                <h1 class="store-title">سيـــدار</h1>
            </div>
            <div class="store-image">
                <img src="/images/stores/sedar.png" alt="">
            </div>
        </div>

        <div class="title">العروض</div>

        <section class="section-offer">
            <OffersCard />
        </section>

        <section class="section-contact">
            <div class="title">بيانات الإتصال</div>
            <div class="contact-container">

                <div class="contact">
                    <div class="contact_info">
                        <i class="fa-brands fa-facebook"></i>
                        <h1>فيسبوك</h1>
                    </div>
                    <div class="contact_info">
                        <i class="fa-brands fa-instagram"></i>
                        <h1>إنستجرام</h1>
                    </div>
                    <div class="contact_info">
                        <i class="fa-brands fa-tiktok"></i>
                        <h1>تيك توك</h1>
                    </div>
                </div>

                <div class="contact">
                    <div class="contact_info">
                        <i class="fa-solid fa-phone"></i>
                        <h1>0123456789</h1>
                    </div>
                    <div class="contact_info">
                        <i class="fa-brands fa-whatsapp"></i>
                        <h1>واتساب</h1>
                    </div>
                    <div class="contact_info">
                        <i class="fa-solid fa-location-dot"></i>
                        <h1>المكان علي الخريطة</h1>
                    </div>
                </div>

            </div>
            <div v-if="isJobs">
                <div class="title">الوظائف </div>
                <div class="jobs-container">
                    <div class="job-image">
                        <img src="/images/job.png" alt="">
                    </div>
                    <div class="job-content">
                        <h1>يحتاج موظفين</h1>
                        <h3>يرجي التواصل مع ادارة المتجر للحصول علي الوظيفة</h3>
                    </div>
                </div>
            </div>

        </section>

        <div class="title">المنتجات</div>

        <section class="section-offer">
            <OffersCard />
        </section>

    </main>

</template>

<script setup>
const isJobs = ref(true)
</script>

<style scoped>
main {
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
}

.store-container {
    position: relative;
    display: inline-block;
    width: 450px;
    height: 100px;
    margin-top: 6rem;
}

.store-name {
    width: 100%;
    height: 100px;
    background-color: var(--primary-orange);
    border-radius: 50px 0 0 50px;
    -webkit-mask-image: linear-gradient(to left, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 20%);
    mask-image: linear-gradient(to left, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 20%);
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

.store-title {
    font-size: 2.7rem;
    font-weight: 900;
    color: var(--white);
    margin-left: 3rem;
}

.store-image {
    position: absolute;
    width: 150px;
    height: 150px;
    background-color: var(--primary-orange);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 100;
    top: 50%;
    right: 70px;
    transform: translateY(-50%);
}

.store-image img {
    width: 70%;
}

.title {
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

.contact-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin: 2rem 1rem;
}

.contact_info {
    display: flex;
    align-items: center;
    gap: 1rem;
    color: var(--primary-dark);
    font-size: 1.5rem;
}

.jobs-container {
    display: flex;
    margin: 0 auto 60px auto;
    width: 60%;
    justify-content: center;
    align-items: center;
    gap: 1rem;
}

.job-image {
    width: 20%;
    height: 160px;
    background-color: var(--white);
    border-radius: 0 30px 30px 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    align-items: center
}

.job-image img {
    width: 90%;
}

.job-content {
    width: 70%;
    height: 160px;
    background-color: var(--white);
    border-radius: 30px 0 0 30px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1rem;
    padding: 0 4rem;
    color: var(--primary-dark);
}

.job-content h1 {
    font-size: 1.8rem;
    font-weight: 900;
}

.job-content h3 {
    font-size: 1.3rem;
    font-weight: 400;
}

.section-category {
    padding: 0 1rem;
    width: 100%;
    min-height: 450px;
    margin: 4rem auto 4rem auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 4rem;
}

.section-offer {
    padding: 0 1rem;
    width: 100%;
    margin: 2rem auto 1rem auto;
}

.section-contact {
    background-color: var(--gray-light);
    padding: .5rem 1rem;
    width: 100%;
    margin: 2rem auto 1rem auto;
}

@media (max-width: 1200px) {
    .jobs-container {
        width: 70%;
        gap: .5rem;
    }

    .job-image {
        width: 25%;
    }

    .job-image img {
        width: 80%;
    }

    .job-content {
        width: 75%;
        gap: .2rem;
        padding: 0 1.5rem;

    }
}


@media (max-width: 900px) {
    .jobs-container {
        width: 90%;
        gap: .5rem;
    }

    .job-image {
        width: 25%;
    }

    .job-image img {
        width: 80%;
    }

    .job-content {
        width: 75%;
        gap: .2rem;
        padding: 0 1rem;

    }

    .job-content h1 {
        font-size: 1.8rem;
        font-weight: 900;
    }

    .job-content h3 {
        font-size: 1.3rem;
        font-weight: 400;
    }

}

@media (max-width: 768px) {
    .store-container {
    width: 280px;
    height: 60px;
}

.store-name {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    height: 60px;

}

.store-title {
    font-size: 1.5rem;
    font-weight: 900;
    margin-left: 3rem;
}

.store-image {
    width: 90px;
    height: 90px;
    top: 50%;
    right: 30px;
    transform: translateY(-50%);
}

.store-image img {
    width: 70%;
}


    .title {
        font-size: 1.3rem;
    }

    .contact_info {
        font-size: .8rem;
        gap: .7rem;

    }

    .jobs-container {
        width: 100%;
    }

    .job-image {
        width: 30%;
    }

    .job-image img {
        width: 80%;
    }

    .job-content h1 {
        font-size: 1.4rem;
        font-weight: 900;
    }

    .job-content h3 {
        font-size: 1rem;
        font-weight: 400;
    }



}

@media (max-width: 480px) {
    .store-container {
        width: 280px;
    }
    .store-title {
    font-size: 1.2rem;
    font-weight: 900;
    margin-left: 3rem;
}
}
</style>