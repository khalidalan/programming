---
{"dg-publish":true,"permalink":"/notes/data-structure/asymptotic-notation/"}
---

### التدوينات المقاربة(Asymptotic Notation )

**التدوينات المقاربة** تُستخدم في تحليل الخوارزميات بهدف وصف سلوك الدوال (functions) عندما تقترب المدخلات من اللانهاية. الغرض الرئيسي منها هو معرفة مدى كفاءة الخوارزميات عندما تزداد كمية البيانات أو حجم المدخلات، حيث تساعد في فهم الوقت أو المساحة التي تستهلكها الخوارزمية.

### الأنواع الرئيسية للتدوينات المقاربة:

1. **Big O Notation (O-الكبيرة):**
   - تُستخدم لوصف أسوأ حالة ممكنة للخوارزمية (Worst Case).
   - تُعطي الحد الأقصى من الزمن أو المساحة التي قد تستهلكها الخوارزمية عند تشغيلها.
   - على سبيل المثال، إذا كانت خوارزمية تتطلب \( O(n^2) \)، فهذا يعني أنه في أسوأ الحالات قد تستغرق وقتًا يتناسب مع \( n^2 \) حيث \( n \) هو حجم المدخلات.

   **مثال**:
   ```python
   def print_items(n):
       for i in range(n):
           for j in range(n):
               print(i, j)
   ```
   - الزمن المستهلك هنا هو \( O(n^2) \) لأن هناك تكرارين متداخلين.

2. **Omega Notation (Ω-أوميجا):**
   - تُستخدم لوصف أفضل حالة للخوارزمية (Best Case).
   - تُعطي الحد الأدنى من الزمن أو المساحة التي تستهلكها الخوارزمية عند تشغيلها.
   - إذا كانت الخوارزمية تتطلب \( Ω(n) \)، فهذا يعني أنه في أفضل الحالات ستعمل الخوارزمية بزمن يتناسب مع \( n \).

   **مثال**:
   ```python
   def find_first_element(arr):
       return arr[0]
   ```
   - الزمن المستهلك هنا هو \( Ω(1) \) لأن الوصول إلى العنصر الأول يتم بشكل فوري.

3. **Theta Notation (Θ-ثيتا):**
   - تُستخدم لوصف الزمن أو المساحة الفعلية التي قد تستهلكها الخوارزمية في المتوسط (Average Case).
   - تُعطي تقييمًا دقيقًا يعبر عن كل من أسوأ وأفضل الحالات معًا، حيث تحدد الزمن الذي ستستغرقه الخوارزمية بشكل تقريبي بناءً على حجم المدخلات.
   - على سبيل المثال، إذا كانت خوارزمية تتطلب \( Θ(n \log n) \)، فهذا يعني أن الزمن المتوقع للخوارزمية يتناسب مع \( n \log n \).

   **مثال**:
   ```python
   def merge_sort(arr):
       if len(arr) > 1:
           mid = len(arr) // 2
           L = arr[:mid]
           R = arr[mid:]
           merge_sort(L)
           merge_sort(R)
           i = j = k = 0
           while i < len(L) and j < len(R):
               if L[i] < R[j]:
                   arr[k] = L[i]
                   i += 1
               else:
                   arr[k] = R[j]
                   j += 1
               k += 1
           while i < len(L):
               arr[k] = L[i]
               i += 1
               k += 1
           while j < len(R):
               arr[k] = R[j]
               j += 1
               k += 1
   ```
   - الزمن المستهلك هنا هو \( Θ(n \log n) \) لأنه يتطلب دمج القوائم.

### الخلاصة:

- **Big O (O-الكبيرة):** تصف أسوأ حالة ممكنة.
- **Omega (Ω-أوميجا):** تصف أفضل حالة ممكنة.
- **Theta (Θ-ثيتا):** تصف الحالة المتوسطة أو الزمن الفعلي.

