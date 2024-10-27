---
{"dg-publish":true,"permalink":"/notes/fundamentals/modular-code/"}
---

### الكود المعياري (Modular Code)

#### **الدالة (Function):**
الدالة هي عبارة عن مجموعة من الأوامر والعبارات التي يتم تجميعها في مكان واحد ويتم تنفيذها عند استدعائها. هناك نوعان من الدوال في البرمجة:

1. **الدوال المدمجة (Built-in Functions):**
   - هي دوال جاهزة للاستخدام وتأتي مع لغة البرمجة، مثل `int()` و `type()` في لغة Python.
  
2. **الدوال المعرفة من قبل المستخدم (User-defined Functions):**
   - هذه هي الدوال التي يقوم المبرمج بإنشائها. فائدتها تكمن في أنها تسهل قراءة الكود وتزيد من إعادة استخدامه، مما يعني أنك تقوم بكتابة الدالة مرة واحدة وتستطيع استخدامها في أماكن متعددة دون تكرار نفس الكود.

#### كتابة الدالة:

الصيغة الأساسية لكتابة الدالة هي كالتالي:

```python
def function_name():
    # الكود المراد تنفيذه داخل الدالة
```

#### مثال:

```python
def my_function():
    print("Hello from a function")

my_function()  # استدعاء الدالة
```

في هذا المثال:
- يتم تعريف الدالة باستخدام الكلمة المفتاحية `def` التي تعني "تعريف".
- `my_function` هو اسم الدالة.
- يتم طباعة "Hello from a function" عند استدعاء الدالة باستخدام `my_function()`.

#### الدوال مع المدخلات (Parameters):

يمكن للدوال أن تستقبل مدخلات، وهي عبارة عن متغيرات يتم تمريرها عند استدعاء الدالة.

الصيغة العامة:

```python
def function_name(parameter):
    # الكود الذي يستخدم المتغير
```

#### مثال:

```python
def my_function(fname, lname):
    print(fname + " " + lname)

my_function("Emil", "Refsnes")
```

في هذا المثال:
- `fname` و `lname` هما مدخلات للدالة.
- عند استدعاء الدالة، يتم تمرير القيم `"Emil"` و `"Refsnes"` لتصبح النتيجة "Emil Refsnes".

#### الدالة التي تُرجع قيمة (Return):

الدالة يمكن أن تعيد قيمة باستخدام الكلمة المفتاحية `return`. القيمة المعادة يمكن استخدامها في دوال أخرى أو عمليات حسابية.

الصيغة العامة:

```python
def function_name(parameter):
    # الكود
    return value  # إرجاع القيمة
```

#### مثال:

```python
def add_numbers(a, b):
    result = a + b
    return result

sum_result = add_numbers(5, 3)
print(sum_result)  # سيطبع 8
```

في هذا المثال:
- يتم تعريف دالة `add_numbers` التي تقوم بجمع الرقمين `a` و `b`، وتعيد النتيجة باستخدام `return`.
- عند استدعاء الدالة وتمرير القيمتين 5 و 3، يتم حفظ النتيجة في المتغير `sum_result`.

#### مثال آخر مع دوال متعددة:

```python
def add_numbers(a, b):
    result = a + b
    return result

def multiply_numbers(x, y):
    multiply_result = x * y
    return multiply_result

sum_result = add_numbers(5, 3)
print(multiply_numbers(5, sum_result))  # سيطبع 40
```

في هذا المثال:
- لدينا دالتان: `add_numbers` لجمع رقمين و `multiply_numbers` لضرب رقمين.
- نتيجة الدالة الأولى `add_numbers` يتم تمريرها كمدخل للدالة الثانية `multiply_numbers`، مما يؤدي إلى ضرب 5 في نتيجة الجمع (8)، ليكون الناتج النهائي 40.