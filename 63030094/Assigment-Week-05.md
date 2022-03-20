# Assignment
 Assignment นี้เป็นการรวม Assignment ของเนื้อหาในสองสัปดาห์ที่เรียนเรื่อง Abstraction  


----
## 1. ให้นำโค้ดต่อไปนี้ไป render ให้เป็น class diagram แล้วนำผลที่ได้มาใส่ใน markdown##
   
   a. ใช้โปรแกรม plantUML บนเว็บ

   b. ใช้ extension ใน VScode
   
   c. ใช้โปรแกรม PlantUML.jar ที่ดาวน์โหลดมาทำงานแบบ offline บนเครื่องของนักศึกษาเอง

### 1.1 Code ของตัวอย่างที่ 3 (สไลด์ที่ 19) ###

``` puml
@startuml 
class Dog{}
class Cat{}
class WhiteAnimals{}
class BlackAnimals{}

WhiteAnimals <|.. whiteCat
WhiteAnimals <|.. whiteDog
BlackAnimals <|.. blackCat
BlackAnimals <|.. blackDog
Cat <|.. whiteCat
Dog <|.. whiteDog
Cat <|.. blackCat
Dog <|.. blackDog
@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 19 ####

![Slide19](./puml-codes/Slide19.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้
![image](https://user-images.githubusercontent.com/92082685/159155751-77799d5e-ecab-4e97-ae32-9d40dc81dcf1.png)

### 1.2 Code ของตัวอย่าง ปรับปรุงการทำ Classification ของหมาและแมว (สไลด์ที่ 20) ###

``` puml
@startuml 
class Dog{}
class Cat{}

Cat <|.. whiteCat
Dog <|.. whiteDog
Cat <|.. blackCat
Dog <|.. blackDog
@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 20 ####

![Slide20](./puml-codes/Slide20.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

![image](https://user-images.githubusercontent.com/92082685/159155773-3d7f53bb-680d-43be-aeef-6e1a1ac769a4.png)


#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสคือการทำ Inheritance ####

``` puml
@startuml 
"Base class" <|-- "Derived class"
@enduml 
```

![Inheritance](./puml-codes/Inheritance-example.png)

![image](https://user-images.githubusercontent.com/92082685/159155973-6f92494d-6187-466c-a6cd-ca87ec4f343c.png)

### 1.3 Classification ของ class คน (สไลด์ที่ 21) ###

``` puml
@startuml 
class Person{
    - Name
    # Lastname
    - Gender
    - Age
    + TellNameAndLastName()
    + TellGender()
    + TellAge()
}

object Somsree
object Somkuan
object Somjit
object Somsak

Person <|.. Somsree
Person <|.. Somkuan
Person <|.. Somjit
Person <|.. Somsak

@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 21 ####


![Slide21](./puml-codes/Slide21.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

![image](https://user-images.githubusercontent.com/92082685/159155856-60312e43-893b-4267-bea0-8247e6da7cb1.png)


#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสและเส้นประคือการทำ Instantiation (สร้างวัตถุ) ####


``` puml
@startuml 
"Base class" <|.. "Derived class"
@enduml 
```
![Instantiation](./puml-codes/Instantiation-example.png)

![image](https://user-images.githubusercontent.com/92082685/159156017-082ba069-dba5-40d3-a8b6-5b50c3238818.png)


### 1.4 การสร้างวัตถุจาก Class คน  (สไลด์ที่ 22) ###

``` puml
@startuml 
class Person{}
object Somsree
object Somkuan
object Somjit
object Somsak

Person <|.. Somsree
Person <|.. Somkuan
Person <|.. Somjit
Person <|.. Somsak

@enduml 
```
#### ตัวอย่างผลที่ได้จากการ render สไลด์ 22 ####

![Slide22](./puml-codes/Slide22.png)

![image](https://user-images.githubusercontent.com/92082685/159156040-8a069114-7dc1-4fa4-8cf7-be79a8d432de.png)


--- 
## 2. ให้แก้ไข code ไฟล์ puml เพื่อให้ได้ภาพตามสไลด์ต่อไปนี้  ##

### 2.1 สไลด์หมายเลข 44 ###

``` puml
@startuml 
class classroom{}
class Whiteboard{}
class Table{}
class Chair{}
class Student{}
class Teacher{}
' Todo: ทำให้สมบูรณ์


@enduml 
```

![image](https://user-images.githubusercontent.com/92082685/159156383-5899082e-c8aa-4612-ab28-bbf29ee6e46e.png)


### 2.2 สไลด์หมายเลข 45 ###

``` puml
@startuml 
class MotorBoat{}
class Car{}
class Helm{}
class Engine{}
class Door{}
class Wheel{}
class SteeringWheel{}
' Todo: ทำให้สมบูรณ์

@enduml 
```

![image](https://user-images.githubusercontent.com/92082685/159156418-16cc79e5-8fbf-4f2e-9226-1596a5609ceb.png)


### 2.3 สไลด์หมายเลข 51 ###

``` puml
@startuml 

class Car{}
class Engine{}
class Wheel{}
class AirConditionner{}

Car <|-- "1..1" Engine
Car <|-- "2..4" Door
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92082685/159156467-9045bd9d-353c-4a82-86ca-530dd5db76ef.png)


#### หมายเหตุ การเขียน cardinality ทำได้โดยใช้รูปแบบดังต่อไปนี้ ####

``` puml
@startuml 
class Car{}
class Engine{}
Car <|-- "1..1" Engine
Car <|-- "2..4" Door
@enduml 
```
ซึ่งจะได้ไดอะแกรมดังรูป

![Cardinality-example](./puml-codes/Cardinality-example.png)


### 2.4 Aggregation ของคลาส หนังสือ  (สไลด์หมายเลข 54) ###

``` puml
@startuml 

class Book{}
class Cover{}
Book <|-- "2..2" Cover
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92082685/159156596-7d19fd35-8527-49c3-9cd5-fb375af27200.png)


### 2.5 เพิ่ม Attribute และ Method ให้กับ Class หนังสือ   (สไลด์หมายเลข 56) ###

``` puml
@startuml 

class Book{
    - ISBN 
    - Name
    + Read()
    + Print()
}
 
' Todo: ทำให้สมบูรณ์

@enduml 
```

![image](https://user-images.githubusercontent.com/92082685/159156635-5bd82dfc-a1e2-4860-847f-d4ba738df280.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###

![image](https://user-images.githubusercontent.com/92082685/159156708-caf4e665-49c1-45ed-9510-923c11c4c9ec.png)


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###

![image](https://user-images.githubusercontent.com/92082685/159156965-4b90db15-c986-4889-afc8-1c544b97254f.png)


### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###

![image](https://user-images.githubusercontent.com/92082685/159156845-d41207f9-40cd-4939-b0fa-759792c2ff75.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###

![image](https://user-images.githubusercontent.com/92082685/159156797-83f77b12-cfb5-45b1-93b7-952b05bd293b.png)


---
