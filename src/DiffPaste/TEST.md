# Diff Paste

`git diff`�� �����ϰ� `-`, `+` ǥ�õ� diff �����͸� ���� Ȱ�� ������ ��Ȯ�� ������ �� �ֽ��ϴ�.


#### �׽�Ʈ ���̽� 1: �ܼ��� ���� �� ����

**���� ����:**
```
line1
line2
line3
line4
```

**Ŭ������ Diff:**
```
 line1
-line2
-line3
+new_line2
+new_line3
 line4
```

**��� ���:**
```
line1
new_line2
new_line3
line4
```

#### �׽�Ʈ ���̽� 2: ���� Hunks (���� ��� ����)

**���� ����:**
```
line1
line2
line3
line4
line5
line6
```

**Ŭ������ Diff:**
```
 line1
-line2
+new_line2
 line3
 line4
-line5
+new_line5
 line6
```

**��� ���:**
```
line1
new_line2
line3
line4
new_line5
line6
```

#### �׽�Ʈ ���̽� 3: ���Ը� �ִ� ���

**���� ����:**
```
line1
line2
line3
```

**Ŭ������ Diff:**
```
 line1
+line1.5
 line2
 line3
```

**��� ���:**
```
line1
line1.5
line2
line3
```

#### �׽�Ʈ ���̽� 4: ������ �ִ� ���

**���� ����:**
```
line1
line2
line3
```

**Ŭ������ Diff:**
```
 line1
-line2
 line3
```

**��� ���:**
```
line1
line3
```

#### �׽�Ʈ ���̽� 5: �߰� ���� �� ����

**���� ����:**
```
line1
line2
line3
line4
line5
```

**Ŭ������ Diff:**
```
 line1
 line2
-line3
+new_line3
+new_line4.1
 line4
 line5
```

**��� ���:**
```
line1
line2
new_line3
new_line4.1
line4
line5
```

#### �׽�Ʈ ���̽� 6: ������ ���� (���� ���԰� ����)

**���� ����:**
```
header1
line1
line2
line3
line4
footer1
footer2
```

**Ŭ������ Diff:**
```
 header1
-line1
+new_line1
 line2
-line3
+new_line3
+added_line3.1
 line4
 footer1
-footer2
+footer2_modified
```

**��� ���:**
```
header1
new_line1
line2
new_line3
added_line3.1
line4
footer1
footer2_modified
```

### �׽�Ʈ ���̽� 7: C# �Լ� ����

**���� ����:**
```csharp
public void FunctionA()
{
    Console.WriteLine("Original Line 1");
    Console.WriteLine("Original Line 2");
}
```

**Ŭ������ Diff:**
```
 public void FunctionA()
 {
-    Console.WriteLine("Original Line 1");
-    Console.WriteLine("Original Line 2");
+    Console.WriteLine("Updated Line 1");
+    Console.WriteLine("Updated Line 2");
 }
```

**��� ���:**
```csharp
public void FunctionA()
{
    Console.WriteLine("Updated Line 1");
    Console.WriteLine("Updated Line 2");
}
```

---

### �׽�Ʈ ���̽� 8: JavaScript �Լ��� �� �ڵ� �߰�

**���� ����:**
```javascript
function greet(name) {
    console.log("Hello, " + name);
    console.log("Have a great day!");
}
```

**Ŭ������ Diff:**
```
 function greet(name) {
     console.log("Hello, " + name);
+    console.log("This is an additional line.");
     console.log("Have a great day!");
 }
```

**��� ���:**
```javascript
function greet(name) {
    console.log("Hello, " + name);
    console.log("This is an additional line.");
    console.log("Have a great day!");
}
```

---

### �׽�Ʈ ���̽� 9: �� ���� ������ �ؽ�Ʈ ����

**���� ����:**
```
This is the first paragraph.

This is the second paragraph.

This is the third paragraph.
```

**Ŭ������ Diff:**
```
 This is the first paragraph.
 
-This is the second paragraph.
+This is the updated second paragraph.
 
 This is the third paragraph.
```

**��� ���:**
```
This is the first paragraph.

This is the updated second paragraph.

This is the third paragraph.
```

---

### �׽�Ʈ ���̽� 10: HTML ���� �� ����

**���� ����:**
```html
<html>
    <body>
        <h1>Title</h1>
        <p>This is a paragraph.</p>
        <footer>Original Footer</footer>
    </body>
</html>
```

**Ŭ������ Diff:**
```
 <html>
     <body>
         <h1>Title</h1>
         <p>This is a paragraph.</p>
-        <footer>Original Footer</footer>
+        <footer>Updated Footer</footer>
     </body>
 </html>
```

**��� ���:**
```html
<html>
    <body>
        <h1>Title</h1>
        <p>This is a paragraph.</p>
        <footer>Updated Footer</footer>
    </body>
</html>
```

### �׽�Ʈ ���̽� 11: JSON ������ ����

**���� ����:**
```json
{
    "name": "John",
    "age": 30,
    "city": "New York"
}
```

**Ŭ������ Diff:**
```
 {
     "name": "John",
-    "age": 30,
+    "age": 31,
     "city": "New York"
 }
```

**��� ���:**
```json
{
    "name": "John",
    "age": 31,
    "city": "New York"
}
```

### �׽�Ʈ ���̽� 12: Python �Լ� ����

**���� ����:**
```python
def calculate(a, b):
    return a + b
```

**Ŭ������ Diff:**
```
 def calculate(a, b):
-    return a + b
+    return a * b
```

**��� ���:**
```python
def calculate(a, b):
    return a * b
```

### �׽�Ʈ ���̽� 13: ���� ��� ���� (������ �ڵ�)

**���� ����:**
```python
def function_one():
    print("Function one start")
    print("Function one end")

def function_two():
    print("Function two start")
    print("Function two end")
```

**Ŭ������ Diff:**
```
 def function_one():
     print("Function one start")
-    print("Function one end")
+    print("Function one modified end")

 def function_two():
     print("Function two start")
-    print("Function two end")
+    print("Function two modified end")
+    print("Additional line for function two")
```

**��� ���:**
```python
def function_one():
    print("Function one start")
    print("Function one modified end")

def function_two():
    print("Function two start")
    print("Function two modified end")
    print("Additional line for function two")
```

### �׽�Ʈ ���̽� 14: �� ���� �ڵ�� �ڵ� ���� ������ Diff

**���� ����:**
```python
def process_data(data):
    print("Starting data processing")
    # Step 1: Clean the data
    cleaned_data = [item.strip() for item in data if item]
    print("Data cleaned")
    
    # Step 2: Transform the data
    transformed_data = [item.upper() for item in cleaned_data]
    print("Data transformed")
    
    # Step 3: Analyze the data
    summary = {
        "count": len(transformed_data),
        "first_item": transformed_data[0] if transformed_data else None,
        "last_item": transformed_data[-1] if transformed_data else None,
    }
    print("Data analyzed")
    
    # Step 4: Save the results
    with open("output.txt", "w") as file:
        file.write("\n".join(transformed_data))
    print("Results saved")
    
    return summary

def helper_function_1():
    print("Helper function 1")

def helper_function_2():
    print("Helper function 2")

def main():
    data = [" item1 ", " item2 ", "item3", None, " item4 "]
    result = process_data(data)
    print(f"Process completed. Summary: {result}")
```

**Ŭ������ Diff:**
```
 def process_data(data):
     print("Starting data processing")
     # Step 1: Clean the data
     cleaned_data = [item.strip() for item in data if item]
     print("Data cleaned")
     
-    # Step 2: Transform the data
-    transformed_data = [item.upper() for item in cleaned_data]
-    print("Data transformed")
+    # Step 2: Transform and filter the data
+    transformed_data = [item.upper() for item in cleaned_data if len(item) > 4]
+    print("Data transformed and filtered")
     
     ... (�ڵ����)
     
     # Step 4: Save the results
-    with open("output.txt", "w") as file:
-        file.write("\n".join(transformed_data))
-    print("Results saved")
+    # Code removed for file saving (external module used)
     
     return summary

...

 def main():
     data = [" item1 ", " item2 ", "item3", None, " item4 "]
-    result = process_data(data)
-    print(f"Process completed. Summary: {result}")
+    # Processing is logged externally, summary is returned for testing
+    return process_data(data)
```

**��� ���:**
```python
def process_data(data):
    print("Starting data processing")
    # Step 1: Clean the data
    cleaned_data = [item.strip() for item in data if item]
    print("Data cleaned")
    
    # Step 2: Transform and filter the data
    transformed_data = [item.upper() for item in cleaned_data if len(item) > 4]
    print("Data transformed and filtered")
    
    # Step 3: Analyze the data
    summary = {
        "count": len(transformed_data),
        "first_item": transformed_data[0] if transformed_data else None,
        "last_item": transformed_data[-1] if transformed_data else None,
    }
    print("Data analyzed")
    
    # Code removed for file saving (external module used)
    
    return summary

...

def main():
    data = [" item1 ", " item2 ", "item3", None, " item4 "]
    # Processing is logged externally, summary is returned for testing
    return process_data(data)
```

### �׽�Ʈ ���� ���� #1

**���� ����:**
```
line1
line2
line1
line2
line3
```

**Ŭ������ Diff:**
```
 line1
-line2
 line3
```

**��� ���:**
```
line1
line2
line1
line3
```

