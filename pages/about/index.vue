<template>
  <div class="about-container">
    <div class="title"> معلومات عنا</div>

    <div class="image-container">
      <img src="/images/mall-interior.jpg" alt="صورة المول" class="main-image">
    </div>

    <section class="section">
      <h2>الصياد بلازا</h2>
      <p>
        مول الصياد يُعد واحدًا من أبرز المشاريع التجارية والسكنية في دمياط القديمة، ويمثل علامة فارقة في مجال الاستثمار
        العقاري بالمدينة. يقع المول على مساحة واسعة تُقدر بـ 10,000 متر مربع، مما يجعله أكبر مول في المنطقة. يتميز
        بتصميم معماري عصري يلبي احتياجات مختلف الفئات، سواء التجارية، الإدارية، أو السكنية.
      </p>
    </section>

    <section class="section">
      <h2>طرق التواصل مع مول الصياد</h2>
      <p>إذا كنت ترغب في معرفة المزيد عن مول الصياد أو حجز وحدات تجارية، إدارية أو سكنية، يمكنك التواصل معنا عبر الطرق
        التالية:
      </p>
      <div class="contact-info">
        <p><i class="fa-solid fa-phone"></i> رقم الهاتف: 0114556789</p>
        <p><i class="fa-solid fa-envelope"></i> البريد الإلكتروني: info@alsayadmall.com</p>
        <p><i class="fa-solid fa-location-dot"></i> العنوان: دمياط القديمة - كورنيش النيل امتداد مبني محافظة دمياط</p>
        <a style=" text-decoration: none; color: var(--primary-dark);" href="https://wa.me/01234567890"
          target="_blank"><i class="fa-brands fa-square-whatsapp"></i> واتساب : 01234567890</a>
      </div>
    </section>

    <section class="section">
      <h2>مكونات مول الصياد</h2>

      <div class="features">
        <div class="feature">
          <h3>الطوابق التجارية</h3>
          <p>
            يتكون المول من 3 طوابق مخصصة بالكامل للأنشطة التجارية.
            يضم مجموعة متنوعة من المتاجر التي تغطي جميع الاحتياجات، مثل الملابس، الأحذية، الإكسسوارات، الإلكترونيات،
            وغيرها
            مساحات مخصصة للمطاعم، حيث يمكن للزوار الاستمتاع بتجربة طعام فريدة.

          </p>
        </div>

        <div class="feature">
          <h3>الأدوار الإدارية</h3>
          <p>
            تم تخصيص بعض الطوابق لتكون مكاتب إدارية وشركات.
            توفر هذه المساحات بيئة عمل مريحة ومجهزة بأحدث التقنيات.
            مثالية للشركات المحلية والدولية التي تبحث عن موقع مركزي في دمياط.

          </p>
        </div>

        <div class="feature">
          <h3>الأدوار السكنية</h3>
          <p>
            الطوابق العليا مخصصة للشقق السكنية، والتي تتميز بتصميمات حديثة ومرافق متكاملة.
            توفر الشقق إطلالات رائعة على المدينة ومساحات واسعة تناسب العائلات.

          </p>
        </div>
      </div>
    </section>

    <section class="section">
      <h2>مزايا مول الصياد</h2>
      <ul class="benefits-list">
        <h4> موقع استراتيجي </h4>
        <li>يقع المول في قلب دمياط القديمة، مما يجعله وجهة مفضلة للسكان والزوار</li>
        <h4>مساحات خضراء</h4>
        <li>يحتوي على مناطق مفتوحة ومساحات خضراء لإضافة لمسة من الراحة والاسترخاء</li>
        <h4>مواقف سيارات</h4>
        <li>يضم المول مواقف سيارات واسعة لتسهيل الوصول للزوار</li>
        <h4>أنظمة أمان حديثة</h4>
        <li>المول مزود بأحدث أنظمة الأمان والمراقبة لتوفير بيئة آمنة للجميع</li>
        <h4>فعاليات موسمية</h4>
        <li>يتم تنظيم أنشطة وفعاليات طوال العام لجذب العائلات والأطفال</li>
      </ul>
    </section>

    <section class="section">
      <h2>أهداف مول الصياد</h2>
      <ul class="goals-list">
        <li>دعم النشاط التجاري في دمياط وزيادة فرص الاستثمار</li>
        <li>توفير تجربة تسوق وترفيه متكاملة للمقيمين والزوار</li>
        <li>تقديم حلول سكنية وإدارية حديثة تناسب جميع الاحتياجات</li>
        <li>إيجاد مكان ترفيهي عائلي متكامل</li>
      </ul>
    </section>
  </div>
</template>

<script setup>


</script>

<style scoped>
.about-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  direction: rtl;
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

.image-container {
  width: 100%;
  margin: 2rem 0;
  overflow: hidden;
  border-radius: 8px;
}

.main-image {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.section {
  margin: 3rem 0;
}

h1 {
  font-size: 2.5rem;
  color: var(--primary-dark);
  text-align: center;
  margin-bottom: 2rem;
}

h2 {
  font-size: 1.8rem;
  color: var(--primary-dark);
  margin-bottom: 1.5rem;
}

h3 {
  font-size: 1.4rem;
  color: var(--primary-dark);
  margin-bottom: 1rem;
}

.contact-info {
  background: var(--gray-light);
  padding: 1.5rem;
  border-radius: 8px;
  margin: 1rem 0;
  font-size: 1.1rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  color: var(--primary-dark);
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.feature {
  background: var(--gray-light);
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.benefits-list,
.goals-list {
  list-style: none;
  padding: 0;
}

.benefits-list li,
.goals-list li {
  margin: 1rem 0;
  padding: 1rem;
  background: var(--gray-light);
  border-radius: 6px;
  position: relative;
  padding-right: 1.5rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.benefits-list li::before,
.goals-list li::before {
  content: "•";
  color: var(--primary-dark);
  font-weight: bold;
  position: absolute;
  right: 0.5rem;
}

@media (max-width: 768px) {
  .about-container {
    padding: 1rem;
  }

  .features {
    grid-template-columns: 1fr;
  }

  h1 {
    font-size: 2rem;
  }

  h2 {
    font-size: 1.5rem;
  }
}
</style>
