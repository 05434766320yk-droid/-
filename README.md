<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ورشة أبو إلياس | تمديدات صحية احترافية</title> حلب وريفها
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #0056b3; /* أزرق داكن */
            --secondary-color: #e9f5ff; /* أزرق فاتح جداً للخلفيات */
            --accent-color: #510; /*احترافية*/
            --text-color: #white; /* لون النصوص الأساسي */
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            color: var(--text-color);
            background-color: var(--secondary-color);
            line-height: 1.6;
        }

        /* الهيدر */
        header {
            background-color: white;
            padding: 15px 30px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 26px;
            font-weight: 700; /* Bold */
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }
        .logo span {
            margin-right: 10px;
            font-size: 30px;
            line-height: 1;
        }

        .btn-call {
            background-color: var(--accent-color);
            color: white;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        .btn-call:hover {
            background-color: #510; /* درجة أغمق عند التحويم */
        }

        /* قسم البطولة (Hero Section) */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.65)), url('https://images.unsplash.com/photo-1576020799627-ae490236a28d?auto=format&fit=crop&w=1400&q=80');
            background-size: cover;
            background-position: center;
            min-height: 85vh; /* ارتفاع أكبر */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 30px;
        }

        .hero h1 { 
            font-size: 3.5rem; 
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.4);
        }
        .hero p { 
            font-size: 1.4rem; 
            max-width: 700px; 
            margin-bottom: 30px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }

        .hero-btn {
            background-color: var(--accent-color);
            color: white;
            padding: 15px 35px;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: background-color 0.3s ease;
        }
        .hero-btn:hover {
            background-color: #510;
        }

        /* قسم الخدمات */
        .services {
            padding: 60px 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: auto;
        }

        .service-card {
            background: white;
            padding: 35px;
            border-radius: 12px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 6px 20px rgba(0,0,0,0.07);
        }

        .service-card:hover { 
            transform: translateY(-12px); 
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }
        .service-icon { 
            font-size: 45px; 
            color: var(--primary-color); 
            margin-bottom: 20px;
        }
        .service-card h3 {
            font-size: 1.7rem;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        .service-card p {
            font-size: 1.05rem;
            color: #666;
        }

        /* قسم لماذا تختارنا */
        .why-us {
            background-color: var(--primary-color);
            color: white;
            padding: 60px 20px;
            text-align: center;
        }
        .why-us h2 {
            font-size: 2.5rem;
            margin-bottom: 40px;
        }
        .advantages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: auto;
        }
        .advantage-item {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .advantage-icon {
            font-size: 50px;
            color: var(--accent-color);
            margin-bottom: 15px;
        }
        .advantage-item h3 {
            font-size: 1.6rem;
            margin-bottom: 10px;
        }
        .advantage-item p {
            font-size: 1.1rem;
            opacity: 0.9;
        }


        /* زر الطوارئ العائم */
        .floating-btn {
            position: fixed;
            bottom: 25px;
            left: 25px;
            background-color: #25d366; /* لون الواتساب */
            color: white;
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 32px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.4);
            text-decoration: none;
            transition: transform 0.2s ease;
            z-index: 1001;
        }
        .floating-btn:hover {
            transform: scale(1.1);
        }

        /* الفوتر */
        footer {
            text-align: center; 
            padding: 30px 20px; 
            background: #222; 
            color: white;
            font-size: 0.95rem;
        }
        footer p {
            margin: 0;
            opacity: 0.8;
        }

        /* استجابة التصميم */
        @media (max-width: 992px) {
            .hero h1 { font-size: 3rem; }
            .hero p { font-size: 1.3rem; }
            .header { padding: 15px 20px; }
            .logo { font-size: 22px; }
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.1rem; }
            .services, .advantages-grid {
                grid-template-columns: 1fr; /* عمود واحد على الجوال */
            }
            .hero { min-height: 70vh; }
            .floating-btn {
                width: 55px;
                height: 55px;
                font-size: 28px;
                bottom: 15px;
                left: 15px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo"><span>👨🏻‍🔧️</span> ورشة أبو إلياس</div>
        <a href="tel:0959602410" class="btn-call">اتصل بنا الآن:  0959602410</a>
    </header>اهلا وسهلا بكم في موقع ورشة ابو الياس في حال لم يتم الرد على الرقم اتصلو بنا على الرقم الاخر 0985893352

    <section class="hero">
        <h1>ورشة أبو إلياس: الحل الأمثل لتمديداتكم الصحية</h1>
        <p>خبراء في تمديدات المياه والصرف الصحي، كشف التسربات، والصيانة الشاملة بأعلى معايير الجودة.</p>
        <a href="#services" class="hero-btn">اكتشف خدماتنا المتكاملة</a>
    </section>

    <section class="services" id="services">
        <div class="service-card">
            <div class="service-icon">💧</div>
            <h3>تمديدات المياه والصرف</h3>
            <p>تصميم وتركيب شبكات المياه والصرف الصحي للمنازل والمباني.</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🔍</div>
            <h3>كشف التسربات</h3>
            <p>تحديد وإصلاح تسربات المياه الخفية بدون تكسير، للحفاظ على ممتلكاتكم.</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🚿</div>
            <h3>تركيب الأدوات الصحية</h3>
            <p>تركيب السخانات، المضخات، الفلاتر، خلاطات المياه، وأطقم الحمامات والمطابخ.</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🛠️</div>
            <h3>صيانة وإصلاح</h3>
            <p>صيانة دورية وإصلاح الأعطال الطارئة بسرعة وكفاءة عالية.</p>
        </div>
    </section>

    <section class="why-us">
        <h2>لماذا تختار ورشة أبو إلياس؟</h2>
        <div class="advantages-grid">
            <div class="advantage-item">
                <div class="advantage-icon">✅</div>
                <h3>الجودة والضمان</h3>
                <p>نلتزم بتقديم خدمات عالية الجودة مع ضمان على جميع أعمالنا.</p>
            </div>
            <div class="advantage-item">
                <div class="advantage-icon">⏱️</div>
                <h3>السرعة والاستجابة</h3>
                <p>فريق عمل جاهز للطوارئ والاستجابة السريعة لطلباتكم.</p>
            </div>
            <div class="advantage-item">
                <div class="advantage-icon">💰</div>
                <h3>أسعار تنافسية</h3>
                <p>نقدم أفضل الخدمات بأقل التكاليف مع الحفاظ على الجودة.</p>
            </div>
            <div class="advantage-item">
                <div class="advantage-icon">👨‍🔧</div>
                <h3>فريق متخصص</h3>
                <p>سباكون ذوو خبرة وكفاءة عالية ومدربون على أحدث التقنيات.</p>
            </div>
        </div>
    </section>

    <a href="https://wa.me/+963959602410" class="floating-btn" target="_blank">💬</a>

    <footer style="text-align: center; padding: 30px; background: #222; color: white;">
        <p>ورشة أبو إلياس © 2024. جميع الحقوق محفوظة.</p>
        <p>للتواصل: 0959602410
       0985893352 |
       https://www.facebook.com/groups/1763108070998952/?ref=share&mibextid=NSMWBT</p>
    </footer>

</body>
</html>
