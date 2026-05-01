# 🏫 بوابة مدرسة سعد بن أبي وقاص الرسمية للغات

<div align="center">

**منصة رقمية تعليمية ذكية**  
*إدارة الفشن التعليمية – محافظة بني سويف*

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://ahimaad.github.io/saadschool/)
[![Firebase](https://img.shields.io/badge/Firebase-Realtime-orange)](https://firebase.google.com)
[![Cloudinary](https://img.shields.io/badge/Cloudinary-Upload-blue)](https://cloudinary.com)
[![Mobile Ready](https://img.shields.io/badge/Mobile-Responsive-gold)]()

</div>

## ✨ الميزات الرئيسية

- **نظام بوستات متكامل** (مثل فيسبوك): كتابة، صور، فيديو، يوتيوب، PDF – مع إعجابات وتعليقات ومشاركة واتساب.
- **شريط أخبار متحرك** (تيكر) تتحكم فيه الإدارة.
- **نتائج الطلاب** مع شهادة أنيقة بها توقيعات الثلاثة (رئيس كنترول، رئيس لجنة، مدير المدرسة) – طباعة PDF ومشاركة واتساب.
- **رفع نتائج بصيغة JSON** لجميع الصفوف دفعة واحدة.
- **الموارد التعليمية** حسب الصفوف (من ثالث ابتدائي إلى ثالث إعدادي) مع منشورات خاصة بكل صف، تظهر اسم المعلم وصورته.
- **الأنشطة المدرسية** (تربية فنية، صحافة، رياضة، مكتبات، تكنولوجيا) بمنشورات منفصلة لكل نشاط مع اسم ووظيفة الناشر.
- **وضع مظلم / فاتح** (Dark/Light mode).
- **لوحة إدارة آمنة** بكلمة سر مشفرة عبر GitHub Secrets.
- **رفع صور وفيديوهات مباشرة إلى Cloudinary** وعرضها داخل الصفحة.
- **تصميم ملكي فخم** بألوان ذهبية، ومتجاوب مع الجوال والتابلت والكمبيوتر.

## 🛠️ التقنيات المستخدمة

| التقنية | الاستخدام |
|---------|-----------|
| **HTML5 / CSS3 / JS** | الواجهة الأساسية |
| **Bootstrap 5 + Swiper.js** | التصميم المتجاوب والسلايدر |
| **Firebase Realtime Database** | تخزين كل البيانات (المنشورات، النتائج، الأخبار، المستخدمين) |
| **Cloudinary** | رفع وتخزين الصور والفيديوهات سحابياً |
| **GitHub Actions** | النشر التلقائي وحقن الأسرار (Secrets) |
| **html2canvas + jsPDF** | طباعة شهادة النتائج كـ PDF |
| **SweetAlert2** | تنبيهات جميلة |

## 🗂️ هيكل قاعدة البيانات (Firebase)

```json
{
  "school_stats": { "studentsCount":1250, "teachersCount":85, "activitiesCount":24 },
  "ticker_news": { "id1": { "text":"خبر", "timestamp": ... } },
  "posts": { ... },  // منشورات الصفحة الرئيسية
  "educational_resources": {
    "p3": { "posts": { ... } },
    "p4": { "posts": { ... } },
    ...  // حتى m3 (ثالث إعدادي)
  },
  "activities": {
    "art": { "posts": { ... } },
    "journalism": { "posts": { ... } },
    "sports": { "posts": { ... } },
    "libraries": { "posts": { ... } },
    "technology": { "posts": { ... } }
  },
  "results": {
    "p6": { "1001": { "name":"أحمد", "subjects":{...}, "total":360, "percentage":90, "grade":"ممتاز" } }
  }
}
