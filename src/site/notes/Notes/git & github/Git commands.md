---
{"dg-publish":true,"permalink":"/notes/git-and-github/git-commands/"}
---

### أهم أوامر Git:

#### 1. **git init**
- يقوم بإنشاء مستودع جديد (Repository) في المجلد الحالي.
  
```bash
git init
```

#### 2. **git add**
- يضيف الملفات إلى منطقة الانتظار (Staging Area) تمهيدًا لحفظ التغييرات.
  
```bash
# إضافة ملف محدد
git add filename.txt

# إضافة جميع الملفات المعدلة
git add .
```

#### 3. **git commit**
- يحفظ التغييرات التي تمت إضافتها إلى منطقة الانتظار بشكل دائم مع رسالة توضيحية.

```bash
git commit -m "رسالة توضيحية عن التعديلات"
```

#### 4. **git status**
- يعرض حالة المستودع، ويبين الملفات التي تم تعديلها والتي تحتاج إلى إضافة أو حفظ.

```bash
git status
```

#### 5. **git log**
- يعرض سجل التعديلات (Commits) التي تم إجراؤها في المستودع.

```bash
git log
```

#### 6. **git clone**
- يقوم باستنساخ مستودع موجود على الإنترنت إلى جهازك.

```bash
git clone https://github.com/username/repository.git
```

#### 7. **git push**
- يقوم برفع التعديلات إلى المستودع البعيد (Remote Repository) مثل GitHub.

```bash
git push origin main
```

#### 8. **git pull**
- يقوم بسحب آخر التعديلات من المستودع البعيد إلى جهازك المحلي.

```bash
git pull origin main
```

#### 9. **git branch**
- يعرض الفروع (Branches) الموجودة في المستودع. يمكن استخدامه أيضًا لإنشاء فرع جديد.

```bash
# عرض جميع الفروع
git branch

# إنشاء فرع جديد
git branch branch-name
```

#### 10. **git checkout**
- يستخدم للتنقل بين الفروع أو لإرجاع التعديلات إلى حالة سابقة.

```bash
# التبديل إلى فرع آخر
git checkout branch-name

# الرجوع إلى commit سابق
git checkout commit-hash
```

#### 11. **git merge**
- يستخدم لدمج فرع مع فرع آخر.

```bash
git merge branch-name
```

#### 12. **git remote**
- يستخدم لإدارة المستودعات البعيدة (Remote Repositories).

```bash
# إضافة مستودع بعيد
git remote add origin https://github.com/username/repository.git
```

#### 13. **git diff**
- يعرض الفروقات بين الملفات التي تم تعديلها ولم يتم إضافتها بعد.

```bash
git diff
```

#### 14. **git reset**
- يستخدم لإلغاء التعديلات التي تم إضافتها إلى منطقة الانتظار أو لإعادة الحالة إلى commit سابق.

```bash
# إعادة الملفات من منطقة الانتظار
git reset

# إعادة المستودع إلى commit معين
git reset --hard commit-hash
```

#### 15. **git stash**
- يحفظ التعديلات الحالية مؤقتًا في قائمة جانبية دون حفظها في commit، للسماح لك بالعمل على شيء آخر.

```bash
git stash
```

#### 16. **git switch**
- يستخدم للتنقل بين الفروع بطريقة مشابهة لـ `git checkout` ولكنه أسهل في الاستخدام ويعتبر أحدث.

```bash
# التبديل إلى فرع موجود
git switch branch-name

# إنشاء فرع جديد والتبديل إليه
git switch -c new-branch-name
```

#### 17. **git rm**
- يستخدم لإزالة الملفات من المستودع ومن نظام الملفات.

```bash
# حذف ملف من المستودع
git rm filename.txt

# حذف ملف من المستودع مع الاحتفاظ بنسخة على جهازك
git rm --cached filename.txt
```

#### 18. **git stash apply**
- يستخدم لاسترجاع التعديلات التي تم حفظها مؤقتًا باستخدام `git stash`.

```bash
# استرجاع آخر تعديلات محفوظة مؤقتًا
git stash apply
```

#### 19. **git stash list**
- يعرض قائمة بجميع التعديلات المحفوظة مؤقتًا باستخدام `git stash`.

```bash
git stash list
```

#### 20. **git rebase**
- يستخدم لدمج التعديلات من فرع إلى فرع آخر بطريقة أكثر تنظيماً مقارنة بـ `git merge`.

```bash
# إعادة الأساس لفرع على فرع آخر
git rebase branch-name
```

#### 21. **git revert**
- يستخدم لإلغاء commit معين عن طريق إنشاء commit جديد يلغي التعديلات التي تمت في commit السابق.

```bash
git revert commit-hash
```

#### 22. **git ignore (.gitignore)**
- يستخدم لتحديد الملفات أو المجلدات التي لا ترغب في تتبعها في مستودع Git. يتم إنشاؤه كملف `.gitignore` في المجلد الرئيسي للمشروع.

```bash
# ملف .gitignore
node_modules/
*.log
*.tmp
```

#### 23. **git tag**
- يستخدم لإنشاء علامة (Tag) على إصدارات معينة من المشروع، مما يسهل العودة إليها لاحقًا.

```bash
# إنشاء علامة على إصدار معين
git tag v1.0

# عرض جميع العلامات
git tag

# إرسال العلامات إلى المستودع البعيد
git push origin --tags
```

#### 24. **git fetch**
- يستخدم لجلب التحديثات من المستودع البعيد دون دمجها مع المستودع المحلي. يتيح لك استعراض التحديثات قبل تطبيقها.

```bash
git fetch origin
```

#### 25. **git cherry-pick**
- يسمح لك بتطبيق commit معين من فرع آخر إلى الفرع الحالي.

```bash
git cherry-pick commit-hash
```

#### 26. **git blame**
- يستخدم لمعرفة من قام بتعديل كل سطر في ملف معين ومتى تم ذلك.

```bash
git blame filename.txt
```

#### 27. **git clean**
- يستخدم لإزالة الملفات غير المتعقبة من مجلد العمل.

```bash
# إزالة الملفات غير المتعقبة
git clean -f

# إزالة الملفات والمجلدات غير المتعقبة
git clean -fd
```

#### 28. **git reflog**
- يعرض سجل كامل لجميع العمليات التي تمت على المستودع، حتى تلك التي لا تظهر في `git log`.

```bash
git reflog
```

#### 29. **git config**
- يستخدم لتكوين إعدادات Git، مثل إعداد معلومات المستخدم أو تكوين تفضيلات خاصة بالمشروع.

```bash
# تعيين اسم المستخدم للبريد الإلكتروني
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# عرض جميع الإعدادات
git config --list
```

#### 30. **git diff --staged**
- يعرض الفروقات بين الملفات التي تم إضافتها إلى منطقة الانتظار (Staging Area) فقط.

```bash
git diff --staged
```

---

هذه الأوامر المتقدمة ستساعدك على التحكم بشكل أفضل في المستودع وتطبيق العمل بشكل أكثر احترافية.