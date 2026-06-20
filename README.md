# Yah Hosting — منصة توقيع عقود الإيجار

موقع جاهز للنشر: المضيف يعبّي بيانات الإيجار ← يطلع رابط يرسله للعميل ← العميل يصادق ويوقّع ← يوصل العقد PDF لإيميل المؤجّر. الرابط يُستخدم مرة واحدة. **بدون قاعدة بيانات.**

الملفات: `index.html` (الموقع) · `api/send.js` (إرسال الإيميل) · `api/lock.js` (قفل الرابط).

> كل الحسابات لازم تكون باسم يحيى وبإيميله **yahya_1420@outlook.com**.

## ١) Resend (مفتاح الإيميل)
1. resend.com ← سجّل بإيميل **yahya_1420@outlook.com**.
2. فعّل من رسالة التحقق ← API Keys ← Create API Key ← انسخ المفتاح (`re_...`).

## ٢) GitHub (رفع الملفات)
1. github.com/new ← الاسم: `yah-hosting` ← Create.
2. Add file ← Upload files ← ارفع `index.html` ومجلّد `api` (داخله `send.js` و `lock.js`).
   تأكّد أن `send.js` و `lock.js` **داخل مجلّد `api`**.

## ٣) Upstash (قفل الرابط)
1. vercel.com (بعد إنشاء المشروع بالخطوة ٤) ← Storage ← Upstash ← Redis ← أنشئ مخزن (مثل `yah-locks`).
2. اربطه بالمشروع (**Connect to Project**) — يضيف `KV_REST_API_URL` و `KV_REST_API_TOKEN` تلقائياً.

## ٤) Vercel (النشر)
1. vercel.com (دخول بـ GitHub) ← Add New → Project ← استورد `yah-hosting`.
2. Project Name: `yah-hosting`.
3. Environment Variables ← أضف `RESEND_API_KEY` = مفتاح Resend.
4. Deploy.

الرابط: **https://yah-hosting.vercel.app**

## الاستخدام
افتح الرابط ← اختر شقة، عبّي التفاصيل ← إنشاء رابط العميل ← أرسله واتساب. العميل يوقّع، ويصلك العقد PDF على إيميلك. توقيع يحيى مثبّت ويظهر بكل عقد.

## تعديل لاحق
الشقق والأسعار وبيانات المؤجّر بأعلى `index.html` (`APTS` و `LESSOR`).
