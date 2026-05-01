# 🏫 منصة مدرسة سعد بن أبي وقاص الرقمية

منصة تعليمية متكاملة تشبه فيسبوك + نظام تعليمي.

## ✨ الميزات
- منشورات مع صور، فيديو، يوتيوب، PDF
- إعجابات، تعليقات، مشاركة واتساب
- أنشطة مدرسية بمنشورات خاصة
- نتائج الطلاب مع شهادة PDF
- رفع نتائج بصيغة JSON
- شريط أخبار متحرك تتحكم به الإدارة
- تصميم ملكي متجاوب، وضع ليلي/فاتح
- إدارة آمنة بكلمة سر مشفرة

## 🔧 التقنيات
- Firebase (Realtime Database)
- Cloudinary (رفع الملفات)
- GitHub Actions (نشر آمن)

## 🚀 النشر
1. أضف Secrets في GitHub:
   - Firebase: `FIREBASE_API_KEY`, `FIREBASE_AUTH_DOMAIN`, `FIREBASE_DATABASE_URL`, `FIREBASE_PROJECT_ID`, `FIREBASE_MESSAGING_SENDER_ID`, `FIREBASE_APP_ID`, `ADMIN_SECRET_KEY`
   - Cloudinary: `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_UPLOAD_PRESET`
2. ارفع الملفات.
3. سيتم النشر تلقائياً.

---
**كلمة السر الافتراضية للمدير**: ستحددها في `ADMIN_SECRET_KEY` (يتم تشفيرها بـ Base64).