---
{"dg-publish":true,"permalink":"/notes/git-and-github/version-control/"}
---

### ما هو Version Control؟
**إدارة الإصدارات (Version Control)** هي أداة تتيح للمبرمجين إدارة وتتبع التغييرات التي تطرأ على الأكواد والملفات في المشاريع البرمجية بمرور الوقت. تعد من الأدوات المهمة خاصةً في تطوير المشاريع الكبيرة التي يعمل عليها أكثر من شخص. 

- **ما الذي يفعله Version Control؟**
  - يسمح لك بتتبع التعديلات على الملفات.
  - يمكّنك من العودة إلى الإصدارات السابقة إذا حدث خطأ ما.
  - يتيح التعاون بين فريق عمل من خلال مشاركة التعديلات والمراجعة عليها.


### Git Init: بدء مستودع جديد
أمر `git init` يستخدم لإنشاء مستودع (Repository) جديد. يمكن استخدامه لبدء تتبع التعديلات في مشروعك الحالي أو بدء مشروع جديد.

#### مثال:
```bash
# إنشاء مستودع جديد
git init
```
عند تنفيذ هذا الأمر، سيتم إنشاء مجلد يسمى `.git` يحتوي على جميع البيانات التي تتعلق بإدارة الإصدارات في مشروعك.

### Git Add: إضافة الملفات إلى منطقة الانتظار
**Git Add** هو أمر يتيح لك إضافة الملفات التي تريد تتبعها إلى منطقة الانتظار (Staging Area). فقط الملفات التي تم إضافتها إلى هذه المنطقة سيتم تضمينها في التعديل القادم (Commit).

#### مثال:
```bash
# إضافة ملفات محددة
git add file1.txt file2.txt

# إضافة جميع الملفات في المشروع
git add .
```
### Git Commit: حفظ التعديلات
**Git Commit** يستخدم لحفظ التعديلات التي تمت إضافتها إلى منطقة الانتظار بشكل دائم في المستودع. كل عملية `Commit` تمثل نقطة محددة في تاريخ المشروع يمكنك الرجوع إليها في أي وقت.

#### مثال:
```bash
# إنشاء commit مع رسالة توضيحية
git commit -m "أضفت ملفات جديدة"
```

### Git Log: عرض سجل التعديلات
أمر `git log` يتيح لك عرض جميع التعديلات السابقة التي تم حفظها في المستودع.

#### مثال:
```bash
# عرض سجل التعديلات
git log
```
يظهر هذا الأمر قائمة بكل التعديلات التي تمت على المشروع، مع عرض معلومات مثل معرف `Commit`، واسم المساهم، والتاريخ، والرسالة التوضيحية.

### Gitignore: تجاهل الملفات غير الضرورية
**Gitignore** هو ملف يحتوي على قائمة بالملفات والمجلدات التي يجب على Git تجاهلها وعدم تتبعها. يستخدم عادة لتجنب تتبع الملفات المؤقتة أو الملفات التي تحتوي على معلومات حساسة.

#### مثال:
```bash
# محتويات ملف .gitignore
node_modules/
*.log
.env
```
في هذا المثال، سيتم تجاهل مجلد `node_modules`، جميع الملفات التي تنتهي بامتداد `.log`، وملف `.env`.
