# Generate Random Number 🤡
ใน tutorial นี้คุณจะได้เรียนรู้เกี่ยวกับการสุ่มตัวเลขในภาษา Dart เราจะแนะนำให้คุณรู้จักกับ Built-in เมธอดของภาษาที่เราสามารถใช้สำหรับสุ่มตัวเลขในภาษาDart 

## เนื้อหาในหัวข้อนี้ ##
- การสุ่มตัวเลขด้วยคลาส Random
- การสุ่มตัวเลขจาก 1-100
- การสุ่มตัวเลขจากช่วงที่กำหนด min,max


 ## 1). การสุ่มตัวเลขด้วยคลาส Random
 คลาส Random ใช้สร้างค่าสุ่มใน Dart จากไลบรารี dart:math เราสามารถสร้างค่า boolean, integer หรือ double สุ่มได้โดยใช้คลาสนี้

 - โดยแบ่งเป็นการสร้างแบบ 2 แบบคือ
### แบบที่ 1 คือ Random([int? seed]) ###
   คือ ตัวสร้าง (constructor) ของคลาส Random ในภาษา Dart ที่ใช้สร้าง random number generator โดยมีพารามิเตอร์ชื่อ seed เป็นค่าทางเลือกที่คุณสามารถระบุได้ พารามิเตอร์ seed นี้ถูกใช้เพื่อกำหนดค่าเริ่มต้นของสถานะ random number generator ซึ่งจะทำให้ค่าที่สุ่มออกมามีลักษณะและลำดับที่สอดคล้องกันหากกำหนด seed

`Example`
 ```dart    
import 'dart:math';

void main() {
   print("Using Random()");
   Random r1 = new Random();
   print(r1.nextInt(100)); //จะทำการสุ่มตััวเลขตั้งแต่ 0-100
   print(r1.nextBool());   //จะทำการสุ่มค่า boolean
   print(r1.nextDouble()); //จะทำการสุ่มเลขทศนิยม
}
```
<details>
  <summary><strong>Output</strong></summary>
  <pre><code>Program continues after than assert</code></pre>
</details>

```dart  
Using Random()
37
fasle
0.6111862138481076
```
   ### แบบที่ 2 คือ Random.secure() 
 คือ Random.secure() ใช้ สร้างrandom number generator ที่มีความสามารถในการสร้างตัวเลขสุ่มที่เหมาะสำหรับการใช้งานทางความปลอดภัย โดยใช้แหล่งเอนโทรปีที่มีความสามารถในการสร้างตัวเลขสุ่มที่มีความสามารถเพิ่มเติมเหมือนในการทำงานเรื่องความปลอดภัย

 `Example`
 ```dart    
import 'dart:math';

void main() {
   print("\nUsing Random.secure() :");
   Random r2 = new Random.secure();
   print(r2.nextInt(100));
   print(r2.nextBool());
   print(r2.nextDouble());
}
```
<details>
  <summary><strong>Output</strong></summary>
  <pre><code>Program continues after than assert</code></pre>
</details>

```dart  
Using Random.recure()
29
true
0.9837051540291097
```

