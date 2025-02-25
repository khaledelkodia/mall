<template>
    <main>
        <StoreLogo />
            <div class="product-container">
                <div class="product-details">
                    <div class="product-gallery">
                        <div class="main-image">
                            <img :src="selectedImage" alt="ساعة كلاسيكية" />
                        </div>
                        <div class="thumbnail-gallery">
                            <img v-for="(image, index) in images" :key="index" :src="image"
                                :class="{ active: selectedImage === image }" @click="selectedImage = image"
                                alt="صورة مصغرة" />
                        </div>
                    </div>
                    <div class="product-info">
                        <h1>ساعة كلاسيكية صناعة صيني هاي كوبي بماكينة يابانية</h1>
                        <div style="display: flex; align-items: center; gap: 30px; width: 100%;">
                            <div class="price">
                            <span class="amount">1600</span>
                            <span class="currency">جنية</span>
                            
                        </div>
                            <button class="order-btn">طلب المنتج</button>
                        </div>
                        
                        
                        <p class="description">
                            ساعة كلاسيكية أنيقة تجمع بين التصميم الراقي والجودة العالية. مصنوعة في الصين بمهارة فائقة.
                            تتميز بأنها هاي كوبي تضاهي الساعات الأصلية. تحتوي على ماكينة يابانية عالية الدقة لضمان أداء
                            ممتاز وموثوقية طويلة الأمد. تصميمها الكلاسيكي يناسب جميع المناسبات، مما يجعلها خيارًا
                            مثاليًا لعشاق الأناقة والبساطة.
                        </p>
                        
                    </div>
                </div>
            </div>
    </main>
</template>

<script setup>
import { ref } from 'vue'

const images = [
    '/images/products/watch.png',
    '/images/products/vacuum.png',
    '/images/products/shirt.png',
    '/images/products/jacket.png'
]

const selectedImage = ref(images[0])
</script>

<style scoped>
main {
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
}

.product-container {
    margin: 4rem 0;
}

.product-details {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
}

.product-gallery {
    display: flex;
    flex-direction: row-reverse;
    gap: 20px;
}

.main-image {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 30px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    background-color: var(--gray-light);
    width: 600px;
    height: 600px;  
}

.main-image img {
    width: 90%;
    
    object-fit: cover;
}

.thumbnail-gallery {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.thumbnail-gallery img {
    width: 80px;
    height: 80px;
    object-fit: cover;
    border-radius: 8px;
    cursor: pointer;
    border: 2px solid transparent;
    transition: border-color 0.3s;
}

.thumbnail-gallery img.active {
    border-color: #FFB800;
}

.product-info {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.product-info h1 {
    font-size: 40px;
    font-weight: 900;
    color: #333;
    margin: 0;
}

.price {
    font-size: 40px;
    font-weight: 900;
    color: var(--white);
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    align-items: center;
    background-color: var(--primary-dark);
    border-radius: 20px;   
    padding: 0.5rem 1rem;
    width: 30%;
    height: 70px;
}

.currency {
    font-size: 20px;
    color: var(--white);
}

.description {
    color: var(--primary-dark);
    font-size: 22px;
    
}

.order-btn {
    background: #FFB800;
    color: #fff;
    border: none;
    padding: 0px 30px;
    border-radius: 20px;
    font-size: 40px;
    cursor: pointer;
    transition: background 0.3s;
    width: fit-content;
    width: 60%;
    height: 70px;
    font-family: 'tajawal', sans-serif;
    font-weight: 900;
    
}

.order-btn:hover {
    background: #e6a600;
}

/* Responsive Design */
@media (max-width: 1200px) {
    .main-image{
        max-width: 400px;
        max-height: 400px;
        width: 100%;
        height: 100%;
    }
    .product-details {
        grid-template-columns: 1fr 1fr;
    }

    .product-gallery {
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .thumbnail-gallery {
        flex-direction: row;
        justify-content: center;
    }

    .product-info {
        text-align: center;
    }

    .order-btn {
        margin: 0 auto;
        font-size: 28px;
    }
    .price {
        font-size: 30px;
    }
}


@media (max-width: 768px) {
    .main-image{
        max-width: 400px;
        max-height: 400px;
        width: 100%;
        height: 100%;
    }
    .product-details {
        grid-template-columns: 1fr;
    }

    .product-gallery {
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .thumbnail-gallery {
        flex-direction: row;
        justify-content: center;
    }

    .product-info {
        text-align: center;
    }

    .order-btn {
        margin: 0 auto;
        font-size: 28px;
    }
    .price {
        font-size: 30px;
    }
}

@media (max-width: 480px) {
    .thumbnail-gallery img {
        width: 60px;
        height: 60px;
    }

    .product-info h1 {
        font-size: 20px;
    }

    .order-btn {
        margin: 0 auto;
        font-size: 20px;
    }

    .price {
        font-size: 20px;
    }
    .currency {
        font-size: 12px;
    }
}
</style>