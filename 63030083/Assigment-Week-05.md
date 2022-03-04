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


![image](https://user-images.githubusercontent.com/92082798/156373412-6e80fca1-6655-4c51-946c-5b2d7123b7f3.png)


^^^ บันทึกผลของนักศึกษา

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


![image](https://user-images.githubusercontent.com/92082798/156373813-814e7ab3-3691-44fb-aeaf-a80bc79b0620.png)


^^^ บันทึกผลของนักศึกษา


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

#### ผลที่ได้จากการ render สไลด์ 21 ####


![image](https://user-images.githubusercontent.com/92082798/156374068-57f99f61-79b5-4c83-90ec-4b66ee629ea1.png)


^^^ บันทึกผลของนักศึกษา

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


![image](https://user-images.githubusercontent.com/92082798/156374425-ff5bf4d8-2712-4aa5-a998-7b9e121e77ba.png)


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
classroom o-- Whiteboard
classroom o-- Table
classroom o-- Chair
classroom o-- Student
classroom o-- Teacher
@enduml 
```

![image](https://user-images.githubusercontent.com/92082798/156661792-eb1b6000-138d-49aa-99c0-16bf35b19b10.png)


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
MotorBoat o-- SteeringWheel
MotorBoat o-- Engine
Car o-- Engine
Car o-- Door
Car o-- Wheel
Car o-- Helm
@enduml 
```

![image](https://user-images.githubusercontent.com/92082798/156661930-cff90e8b-d6df-4a2f-bebc-5758fdc0cdad.png)


### 2.3 สไลด์หมายเลข 51 ###

``` puml
@startuml 

class Car{}
class Engine{}
class Wheel{}
class AirConditionner{}

Car o-- "1..1" Engine
Car o-- "2..4" Door
Car o-- "4..4" Wheel
Car o-- "0..1" AirConditionner

@enduml 
```

![image](https://user-images.githubusercontent.com/92082798/156662012-2317710a-78cc-4835-ae07-1bd49bbb87e4.png)

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
class Introduction{}
class List{}
class Content{}
class Bibliography{}

Book o-- "2..2" Cover
Book o-- "1..1" Introduction
Book o-- "1..1" List
Book o-- "1..N" Content
Book o-- "1..1" Bibliography

@enduml 
```

![image](https://user-images.githubusercontent.com/92082798/156662252-27315f89-413a-42ae-859c-133b87db34bc.png)

### 2.5 เพิ่ม Attribute และ Method ให้กับ Class หนังสือ   (สไลด์หมายเลข 56) ###

``` puml
@startuml 

class Book{
    - ISBN 
    - Name
    + Read()
    + Print()
}
class Cover{
    + Typecover
    + Open()
}
class Introduction{
    - Textmessage
    - Authorname
    + Read()
}
class List{
    - Textmessage
    + Read()
}
class Content{
    - Chapter
    + Read()
}
class Bibliography{
    - Textmessage
    + Read()
}
class Paper{
    - ContentofPaper
    + Open()
    + Read()
}
class Picture{
    - Image
    + See()
}
class Font{
    - Character
    + Spell()
}
Book o-- Cover
Book o-- Introduction
Book o-- List
Book o-- Content
Book o-- Bibliography
Content o-- Paper
Paper o-- Picture
Paper o-- Font
@enduml  
```
![image](https://user-images.githubusercontent.com/92082798/156662514-67b21495-dbd8-4684-8c36-3b242a4e7edc.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###

![image](https://user-images.githubusercontent.com/92082798/156837392-b2aa67dd-703d-4f10-a2f7-9848434efe89.png)
![image](https://user-images.githubusercontent.com/92082798/156837406-23ce61ef-c4f7-4f54-a285-8f85e3449683.png)


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###

![image](https://user-images.githubusercontent.com/92082798/156838251-032b96e2-2850-4fd4-b6d2-9b4e2387b021.png)
![image](https://user-images.githubusercontent.com/92082798/156838268-0b61532e-3ddd-4f8a-81fd-d1bac80ae98e.png)


### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###

![image](https://user-images.githubusercontent.com/92082798/156838849-107073d4-109c-4922-914b-fe1d1b58cbd9.png)
![image](https://user-images.githubusercontent.com/92082798/156838859-205d1bf3-634a-4371-af7e-37323b513519.png)


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###

![image](https://user-images.githubusercontent.com/92082798/156840496-bcc4f757-3cdd-43d0-b38a-8027cd919fdd.png)
![image](https://user-images.githubusercontent.com/92082798/156840528-9cdc2582-5108-4292-86d6-7514dad74c45.png)


---
