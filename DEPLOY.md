<div dir="rtl">

# نشر موقع النماذج على GitHub Pages

المستودع مُهيّأ محلياً وجاهز للرفع. اتبع الخطوات بالترتيب.

---

## ⚠️ قبل الرفع — خطوة إلزامية

الملف `index.html` فيه **٣ مواضع** تحمل علامات نائبة. استبدلها بمعلوماتك الحقيقية:

| السطر | الحالي | ضع بدلاً منه |
|---|---|---|
| تحت العنوان | `[CONSULTANT_NAME]` | اسمك ومسمّاك |
| في التذييل | `[CONSULTANT_NAME]` | اسمك |
| في التذييل | `05XXXXXXXX` و `name@example.com` | جوالك وبريدك |

ابحث في الملف عن `⚙️` — كل موضع معلّم بها.

> **تسليم ملف فيه `[CONSULTANT_NAME]` يكشف أنه قالب — وهذا أسوأ انطباع ممكن. لا ترفع قبل الاستبدال.**

---

## ١) أنشئ المستودع على GitHub

من المتصفح: <https://github.com/new>

- **الاسم:** `demos` (أو أي اسم تفضّله)
- **الرؤية:** **Public** — إلزامي لتفعيل GitHub Pages مجاناً
- **لا تُضِف** README ولا .gitignore (موجودان محلياً)

---

## ٢) اربط وارفع

نفّذ من داخل مجلد `demo-site`:

```bash
git remote add origin https://github.com/mahboubgs1/demos.git
git branch -M main
git push -u origin main
```

سيطلب منك تسجيل الدخول — استخدم **Personal Access Token** بدل كلمة المرور
(GitHub ألغى كلمات المرور للرفع). أنشئه من: Settings ← Developer settings ← Personal access tokens.

---

## ٣) فعّل GitHub Pages

في صفحة المستودع: **Settings ← Pages**

- **Source:** Deploy from a branch
- **Branch:** `main` · **Folder:** `/ (root)` ← احفظ

بعد ١–٢ دقيقة يصير الرابط جاهزاً:

```
https://mahboubgs1.github.io/demos/
https://mahboubgs1.github.io/demos/mathaq/     ← اللوحة مباشرة
```

---

## ٤) (اختياري لكن يستحق) نطاقك الخاص

رابط باسمك أقوى بكثير من رابط github.io:

1. في مزوّد النطاق أضف سجل `CNAME` باسم `demo` يشير إلى `mahboubgs1.github.io`
2. في **Settings ← Pages ← Custom domain** اكتب `demo.نطاقك.com` واحفظ
3. فعّل **Enforce HTTPS** بعد صدور الشهادة

النتيجة: `https://demo.نطاقك.com/mathaq/`

---

## ٥) التحديث لاحقاً

أي تعديل على الملفات:

```bash
git add -A
git commit -m "وصف التعديل"
git push
```

الموقع يتحدّث تلقائياً خلال دقيقة.

---

## 🔐 ملاحظات مهمة

- **الموقع علني.** أي شخص معه الرابط يفتحه، وقد تفهرسه محركات البحث. هذا مقبول — بل مطلوب — لأن كل البيانات **افتراضية بالكامل** ولا تخص أي عميل.
- **لا ترفع أبداً** ملفات تحتوي بيانات عميل حقيقية إلى مستودع علني.
- **الملفات الداخلية لا تُرفع هنا:** `README.md` و `IDEAS.md` و `BUILD_GUIDE.md` وملفات SQL وورقة جاهزية البيانات — هذه أدوات عملك، لا مواد عرض.
- هوية git في هذا المستودع مضبوطة على `mahboubgs1@users.noreply.github.com` حتى لا يظهر بريدك الشخصي في السجل العلني. لتغييرها:
  ```bash
  git config user.name "اسمك"
  git config user.email "بريدك"
  ```

---

## 🗂️ ماذا يوجد هنا

```
demo-site/
├── index.html        ← صفحة الهبوط (قائمة النماذج)
├── mathaq/index.html ← لوحة سلسلة المقاهي
├── .nojekyll         ← يمنع معالجة Jekyll (ضروري)
└── DEPLOY.md         ← هذا الملف (لا يظهر للزوار)
```

</div>
