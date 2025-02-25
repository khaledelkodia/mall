<template>
    <div class="store-container">
        <div class="store-name">
            <h1 class="store-title">سيـــدار</h1>
        </div>
        <div class="store-image">
            <img src="/images/stores/sedar.png" alt="">
        </div>
    </div>
</template>

<style scoped>
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