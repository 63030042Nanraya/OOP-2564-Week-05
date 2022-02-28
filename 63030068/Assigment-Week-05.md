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

## ผลที่ได้จากการ render สไลด์ 19 ##

#### a. plantUML บนเว็บ
![image](https://user-images.githubusercontent.com/50146617/155973064-2365d3a9-3594-44b6-8e39-0bf8c65ef150.png)
#### b. ใช้ extension ใน VScode
![image](https://user-images.githubusercontent.com/50146617/155973730-80a43a22-41b7-463e-862a-4919000dcf1a.png)
#### c. ใช้โปรแกรม PlantUML.jar
![image](https://user-images.githubusercontent.com/50146617/155974193-18fdd03f-63b0-4fc4-95a2-7cfd6ce2b5ff.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

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

## ผลที่ได้จากการ render สไลด์ 20 ##

#### a. plantUML บนเว็บ
![image](https://user-images.githubusercontent.com/50146617/155974361-17f5b253-6238-41cc-bd26-e527f3e06163.png)
#### b. ใช้ extension ใน VScode
![image](https://user-images.githubusercontent.com/50146617/155974430-c6fa7e50-aeba-4170-960d-ea9c0b2ce277.png)
#### c. ใช้โปรแกรม PlantUML.jar
![image](https://user-images.githubusercontent.com/50146617/155974538-1e5da826-d9c3-4c29-b23a-a16a5ca7be1b.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้


#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสคือการทำ Inheritance ####

``` puml
@startuml 
"Base class" <|-- "Derived class"
@enduml 
```

![Inheritance](./puml-codes/Inheritance-example.png)

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

## ผลที่ได้จากการ render สไลด์ 21 ##

#### a. plantUML บนเว็บ
![image](https://user-images.githubusercontent.com/50146617/155974774-ddf903af-2755-4cbb-bdc3-cb8a8de924a9.png)
#### b. ใช้ extension ใน VScode
![image](https://user-images.githubusercontent.com/50146617/155974857-85d7c5ad-0376-4012-9153-f6c8db6a433f.png)
#### c. ใช้โปรแกรม PlantUML.jar
![image](https://user-images.githubusercontent.com/50146617/155974900-80e8d1fd-32bc-41cc-ae38-0aac8207f500.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสและเส้นประคือการทำ Instantiation (สร้างวัตถุ) ####


``` puml
@startuml 
"Base class" <|.. "Derived class"
@enduml 
```
![Instantiation](./puml-codes/Instantiation-example.png)


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

#### a. plantUML บนเว็บ
![image](https://user-images.githubusercontent.com/50146617/155975144-c53ae5a0-046d-4a69-9472-01516a758ad4.png)
#### b. ใช้ extension ใน VScode
![image](https://user-images.githubusercontent.com/50146617/155975229-f7c6470e-c81c-4d12-889e-f6b8bcce9791.png)
#### c. ใช้โปรแกรม PlantUML.jar
![image](https://user-images.githubusercontent.com/50146617/155975289-85092c2c-08b8-41f4-b78b-8571f233d02c.png)

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


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###


---
