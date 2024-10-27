---
{"dg-publish":true,"permalink":"/notes/beyond-fundamentals/strings/"}
---


#### **جمع السلاسل (Concatenation):**
دمج سلاسل متعددة معًا لتكوين سلسلة واحدة جديدة. يمكن استخدام علامة **`+`** لدمج النصوص.
  
#### **مثال:**
```python
name = "Ali"
age = "22"
country = "Egypt"
result = "Welcome " + name + ". Your age is " + age + ". Your country is " + country
print(result)
# الناتج: Welcome Ali. Your age is 22. Your country is Egypt
```

### **دوال النصوص (String Functions):**
بايثون توفر العديد من الدوال الجاهزة للعمل على النصوص، ويتم استدعاء هذه الدوال على النصوص كالتالي:
  
```python
string_name.function_name()
```

#### **أشهر دوال النصوص:**

- **`capitalize()`**: لجعل أول حرف في السلسلة **Capital**.
  
  **مثال:**
  ```python
  text = "hello world"
  print(text.capitalize())  # الناتج: Hello world
  ```

- **`lower()`**: لجعل جميع الحروف **صغيرة (Lowercase)**.
  
  **مثال:**
  ```python
  text = "HELLO WORLD"
  print(text.lower())  # الناتج: hello world
  ```

- **`find(substring)`**: للبحث عن موقع **كلمة معينة** أو جزء من النص داخل سلسلة.
  
  **مثال:**
  ```python
  text = "Welcome to Python"
  print(text.find("Python"))  # الناتج: 11 (موقع بداية كلمة "Python")
  ```

- **`replace(old, new)`**: لاستبدال **كلمة بكلمة أخرى** داخل السلسلة.
  
  **مثال:**
  ```python
  text = "I like Python"
  print(text.replace("Python", "Java"))  # الناتج: I like Java
  ```

- **`split()`**: تقسيم السلسلة إلى قائمة **List** تحتوي على أجزاء السلسلة التي تم فصلها بناءً على محدد معين.
  
  **مثال:**
  ```python
  text = "apple,banana,orange"
  print(text.split(","))  # الناتج: ['apple', 'banana', 'orange']
  ```

### **ملخص دوال النصوص:**
- `capitalize()`: تحويل الحرف الأول إلى كبير.
- `lower()`: تحويل النص إلى أحرف صغيرة.
- `find()`: إيجاد موقع النص المطلوب.
- `replace()`: استبدال جزء من النص بآخر.
- `split()`: تقسيم النص إلى أجزاء.

هذه الدوال تساعد على معالجة النصوص بسهولة وفعالية في بايثون.