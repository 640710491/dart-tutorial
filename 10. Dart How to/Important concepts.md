# Important concepts
ใน tutorial นี้เราจะมาดูเรื่องแนวคิดที่สำคัญของ Dart  โดยที่ภาษา Dart เป็นภาษาโปรแกรมที่มีแนวคิดแบบ Object-Oriented Programming (OOP) ที่ให้ความสำคัญกับการจัดการกับ Object และ Class และใช้ในสร้าง Applications หรือ Project อื่นๆ และจะต้องคำนึงถึงข้อเท็จจริงและแนวคิดดังนี้
## Objects & Class
ใน Dart นั้นทุกอย่างคือวัตถุ และวัตถุทั้งหมดเป็น instance ของ class ซึ่งรวมถึงตัวเลข ฟังก์ชัน และค่าว่างถือเป็นวัตถุ อ็อบเจ็กต์ทั้งหมดจะสืบทอดมาจากคลาส Object ยกเว้นค่า null ถ้าหากใช้ sound null safety

## Null Safety
Dart เวอร์ชัน 2.12 ขึ้นไปที่เปิดใช้งาน null safety เมื่อประกาศตัวแปรจะต้องระบุว่าตัวแปรนั้นจะมีค่า null ซึ่งหมายความว่าตัวแปรไม่สามารถมีค่าว่างได้ 

### Example : ไม่ระบุค่าของตัวแปร name
```dart
  void main() {
    String name;  
    print(name);  
  }
```
- Output
  
``` dart
Error: Non-nullable variable 'name' must be assigned before it can be used.
```

จากตัวอย่างจะทำให้เกิดการ runtime error หากต้องการระบุว่าตัวแปรอาจมีค่าเป็น null จะต้องเพื่มเครื่องหมายคำถาม ? ไปที่ประเภทข้อมูล 

### Example 
```dart
  void main() {
    String? name;  // ประกาศตัวแปร name โดยระบุว่าอาจจะมีค่าเป็น null
    print(name);  
  }
```
- Output
  
``` dart
null
```