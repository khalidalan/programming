---
{"dg-publish":true,"permalink":"/notes/data-structure/technical-examples-stack/"}
---

### أمثلة تقنية على استخدام الـ Stack

#### 1. **تنفيذ عمليات Undo/Redo**
   - **الوصف**: في التطبيقات، كمعالجة النصوص، يتم استخدام مكدسين (Stacks) لتنفيذ عمليات التراجع (Undo) والإعادة (Redo). يتم تخزين العمليات المنفذة في مكدس التراجع (Undo Stack)، بينما يتم نقل العمليات المُتراجَع عنها إلى مكدس الإعادة (Redo Stack).
   - **مثال في Python**:
     ```python
     undo_stack = []
     redo_stack = []

     # تنفيذ عملية وتخزينها
     action = "Write 'Hello'"
     undo_stack.append(action)  # إضافة العملية لمكدس التراجع

     # التراجع عن عملية
     if undo_stack:
         last_action = undo_stack.pop()  # إزالة آخر عملية
         redo_stack.append(last_action)   # نقل العملية لمكدس الإعادة

     # إعادة العملية
     if redo_stack:
         action_to_redo = redo_stack.pop()  # إزالة آخر عملية من مكدس الإعادة
         undo_stack.append(action_to_redo)  # إعادة العملية لمكدس التراجع
     ```

#### 2. **تنفيذ تحليل الأقواس في عبارات رياضية**
   - **الوصف**: يُستخدم Stack للتحقق من تطابق الأقواس في التعبيرات الرياضية أو البرمجية. يتم وضع الأقواس المفتوحة في المكدس، ويتم التحقق من الأقواس المغلقة بمقارنتها مع آخر قوس مفتوح.
   - **مثال في Python**:
     ```python
     def is_balanced(expression):
         stack = []
         for char in expression:
             if char in "({[":
                 stack.append(char)
             elif char in ")}]":
                 if not stack:
                     return False
                 top = stack.pop()
                 if (char == ")" and top != "(") or \
                    (char == "}" and top != "{") or \
                    (char == "]" and top != "["):
                     return False
         return len(stack) == 0

     # اختبار للتوازن
     print(is_balanced("{[()]}"))  # True
     print(is_balanced("{[(])}"))  # False
     ```

#### 3. **تقييم العبارات الرياضية باستخدام الـ Stack**
   - **الوصف**: عند تقييم تعبير رياضي في التدوين العكسي (Postfix Notation)، يتم دفع الأعداد إلى المكدس وتُجرى العمليات الحسابية باستخدام القيم في المكدس.
   - **مثال في Python**:
     ```python
     def evaluate_postfix(expression):
         stack = []
         for char in expression:
             if char.isdigit():
                 stack.append(int(char))
             else:
                 b = stack.pop()
                 a = stack.pop()
                 if char == '+':
                     stack.append(a + b)
                 elif char == '-':
                     stack.append(a - b)
                 elif char == '*':
                     stack.append(a * b)
                 elif char == '/':
                     stack.append(a / b)
         return stack.pop()

     # مثال على التقييم
     print(evaluate_postfix("231*+9-"))  # الناتج: -4
     ```

#### 4. **إدارة استدعاءات الوظائف في البرمجة (Call Stack)**
   - **الوصف**: عند استدعاء الدوال (Functions) المتداخلة، يتم دفع كل استدعاء إلى المكدس مع بياناته، وعند انتهاء التنفيذ يتم إزالة البيانات واسترجاعها من المكدس، مما يسمح بعودة دالة إلى الأخرى التي استدعتها.
   - **مثال في Python**:
     ```python
     def factorial(n):
         if n == 1:
             return 1
         else:
             return n * factorial(n - 1)

     # المثال يقوم بحساب 5! باستخدام مكدس استدعاءات الوظائف
     print(factorial(5))  # الناتج: 120
     ```

### ملخص
يُعتبر الـ Stack أداة قوية وضرورية في البرمجة، تُستخدم في عدة مهام كالتراجع عن العمليات، التحقق من صحة العبارات، إدارة استدعاءات الدوال، وتقييم العبارات الرياضية.