---
{"dg-publish":true,"permalink":"/notes/data-structure/dynamic-array-operations/"}
---

### **عمليات المصفوفات الديناميكية**

في المصفوفات الديناميكية، يمكن القيام بالعديد من العمليات الأساسية التي تجعل هذا الهيكل مرنًا وفعالًا. دعنا نتحدث عن العمليات التالية بالتفصيل:

---

### 1. **عملية استرجاع عنصر (Access an Element)**

**الوصف:**
تسمح لك هذه العملية بالوصول إلى عنصر معين داخل المصفوفة باستخدام فهرسه (موقعه) الذي يبدأ عادةً من 0.

**التعقيد الزمني:**  
\( O(1) \) لأن الوصول إلى عنصر معين في المصفوفة يكون مباشرًا بناءً على الفهرس.

**مثال في Python:**
```python
my_list = [10, 20, 30, 40, 50]
element = my_list[2]  # استرجاع العنصر في الفهرس 2
print(element)  # الناتج: 30
```

---

### 2. **عملية تغيير قيمة عنصر (Update an Element)**

**الوصف:**
تسمح لك هذه العملية بتحديث أو تعديل قيمة عنصر معين في المصفوفة باستخدام فهرسه.

**التعقيد الزمني:**  
\( O(1) \) لأن تحديث قيمة عنصر يتم مباشرة باستخدام الفهرس.

**مثال في Python:**
```python
my_list = [10, 20, 30, 40, 50]
my_list[1] = 25  # تغيير العنصر في الفهرس 1 إلى 25
print(my_list)  # الناتج: [10, 25, 30, 40, 50]
```

---

### 3. **عملية معرفة عدد العناصر (Get the Number of Elements)**

**الوصف:**
تُستخدم هذه العملية لمعرفة عدد العناصر الموجودة حاليًا في المصفوفة الديناميكية.

**التعقيد الزمني:**  
\( O(1) \) لأن معرفة عدد العناصر يتم بشكل مباشر.

**مثال في Python:**
```python
my_list = [10, 20, 30, 40, 50]
length = len(my_list)  # معرفة عدد العناصر في المصفوفة
print(length)  # الناتج: 5
```

---

### 4. **عملية الإضافة (Add an Element)**

**الوصف:**
تسمح لك هذه العملية بإضافة عنصر جديد إلى نهاية المصفوفة. إذا امتلأت المصفوفة، يتم مضاعفة حجمها تلقائيًا ثم يتم نسخ جميع العناصر القديمة إلى المصفوفة الجديدة.

**التعقيد الزمني:**  
- **أفضل حالة:** \( O(1) \) إذا كانت هناك مساحة كافية لإضافة العنصر.
- **أسوأ حالة:** \( O(n) \) عندما يتم إعادة تخصيص الحجم (عند مضاعفة حجم المصفوفة).

**مثال في Python:**
```python
my_list = [10, 20, 30]
my_list.append(40)  # إضافة عنصر جديد إلى نهاية المصفوفة
print(my_list)  # الناتج: [10, 20, 30, 40]
```

---

### 5. **عملية الحذف (Remove an Element)**

**الوصف:**
تسمح لك هذه العملية بحذف عنصر من المصفوفة إما باستخدام الفهرس أو القيمة. بعد الحذف، يتم تحريك العناصر التالية لتغطية المكان الذي تم حذفه.

**التعقيد الزمني:**  
- **أفضل حالة:** \( O(1) \) إذا تم حذف العنصر من النهاية.
- **أسوأ حالة:** \( O(n) \) إذا تم حذف العنصر من بداية المصفوفة أو من موقع يتطلب إعادة ترتيب العناصر.

**مثال في Python (الحذف باستخدام القيمة):**
```python
my_list = [10, 20, 30, 40, 50]
my_list.remove(30)  # حذف العنصر الذي قيمته 30
print(my_list)  # الناتج: [10, 20, 40, 50]
```

**مثال في Python (الحذف باستخدام الفهرس):**
```python
my_list = [10, 20, 30, 40, 50]
del my_list[1]  # حذف العنصر في الفهرس 1
print(my_list)  # الناتج: [10, 30, 40, 50]
```

---

### **ملخص التعقيد الزمني للعمليات:**

| **العملية**                    | **أفضل حالة** | **أسوأ حالة** |
|---------------------------------|---------------|---------------|
| استرجاع عنصر                   | \( O(1) \)    | \( O(1) \)    |
| تغيير قيمة عنصر                | \( O(1) \)    | \( O(1) \)    |
| معرفة عدد العناصر              | \( O(1) \)    | \( O(1) \)    |
| إضافة عنصر                     | \( O(1) \)    | \( O(n) \)    |
| حذف عنصر                       | \( O(1) \)    | \( O(n) \)    |

---

### **الخلاصة:**

المصفوفات الديناميكية تقدم مرونة كبيرة في التعامل مع البيانات مقارنة بالمصفوفات العادية. يمكن تنفيذ العديد من العمليات بسهولة وكفاءة، ولكن بعض العمليات، مثل الإضافة أو الحذف في منتصف المصفوفة، قد تكون مكلفة من حيث الزمن.