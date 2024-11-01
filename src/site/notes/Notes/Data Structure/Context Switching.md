---
{"dg-publish":true,"permalink":"/notes/data-structure/context-switching/"}
---

## ما هو تبديل السياق؟
- **تبديل السياق (Context Switching)** هو ميزة في **أنظمة التشغيل متعددة المهام**.
- يسمح بتشارك **وحدة المعالجة المركزية (CPU)** بين **عمليات متعددة**.
- عند تبديل السياق، يقوم نظام التشغيل بحفظ حالة العملية الحالية (التعليمات، المتغيرات) ثم يستدعي عملية أخرى لتشغيلها، ويعيد لاحقًا استئناف العملية السابقة من حيث توقفت.

## الفائدة:
- يساعد في تنفيذ عدة مهام في وقت واحد بشكل متزامن، مما يعطي الشعور بأن النظام يعمل بكفاءة مع عدة برامج في نفس الوقت.

---

# (Garbage Collection)

- **جمع القمامة (Garbage Collection)** هو عملية في إدارة الذاكرة يقوم بها **نظام التشغيل** أو **لغة البرمجة**.
- يهدف إلى **تحرير مساحة الذاكرة** المخصصة للكائنات التي لم يعد البرنامج بحاجة إليها.

## الفائدة:
- يساعد في تحسين **إدارة الذاكرة** عن طريق التخلص من الكائنات غير الضرورية، مما يوفر مساحة للبيانات الجديدة ويقلل من احتمالية نفاد الذاكرة.
