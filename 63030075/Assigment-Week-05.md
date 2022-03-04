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

![image](https://user-images.githubusercontent.com/92082233/156373903-94578390-a73d-4d5d-8bc3-35306e24f916.png)

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

#### ผลที่ได้จากการ render สไลด์ 20 ####

![image](https://user-images.githubusercontent.com/92082233/156374154-2bba6385-0633-4897-bbf7-590c07b48381.png)

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

#### ผลที่ได้จากการ render สไลด์ 21 ####

![image](https://user-images.githubusercontent.com/92082233/156374404-fab7e1b8-865c-4371-bd94-b31ec7f00c42.png)

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

![Slide22](./puml-codes/Slide22.png)

--- 
## 2. ให้แก้ไข code ไฟล์ puml เพื่อให้ได้ภาพตามสไลด์ต่อไปนี้  ##

### 2.1 สไลด์หมายเลข 44 ###

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

![image](https://user-images.githubusercontent.com/92082233/156839973-771a5a95-0a76-4b47-a572-364a8b75d367.png)


### 2.2 สไลด์หมายเลข 45 ###

@startuml 
class MotorBoat{}
class Car{}
class Helm{}
class Engine{}
class Door{}
class Wheel{}
class SteeringWheel{}

MotorBoat o-- Helm
MotorBoat o-- Engine

Car o-- Engine
Car o-- Door
Car o-- Wheel
Car o-- SteeringWheel
@enduml 

![image](https://user-images.githubusercontent.com/92082233/156839807-b4f949ae-3046-4388-bfef-a0e0d8da71bf.png)

### 2.3 สไลด์หมายเลข 51 ###

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

![image](https://user-images.githubusercontent.com/92082233/156840181-c8c18870-f50b-4f11-ab10-f2155fcb70a2.png)
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

@startuml 
class Book{}
class Cover{}
class Introduction{}
class Index{}
class Content{}
class Bibliography{}

Book o-- "2..2" Cover
Book o-- "1..1" Introduction
Book o-- "1..1" Index
Book o-- "1..N" Content
Book o-- "1..1" Bibliography
@enduml 

![image](https://user-images.githubusercontent.com/92082233/156838877-e08c9eb6-8c3c-42e5-9b7d-81050b4941e3.png)


### 2.5 เพิ่ม Attribute และ Method ให้กับ Class หนังสือ   (สไลด์หมายเลข 56) ###
@startuml 
class Book{
    - ISBN 
    - Name
    + Read()
    + Print()
}

class Cover{
    + CoverType
    + Flip()
}

class Introduction{
    - TextMessage
    - AuthorName
    + Read()
}

class Index{
    - TextMessage
    + Read()
}

class Chapter{
    - ContentofChapter
    + Read()
}

class Bibliography{
    - TextMessage
    + Read()
}

class Page{
    - ContentofPage
    + Flip()
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
Book o-- Index
Book o-- Chapter
Book o-- Bibliography
Chapter o-- Page
Page o-- Picture
Page o-- Font
@enduml  

![image](https://user-images.githubusercontent.com/92082233/156839586-272ce28a-be21-4522-bd9b-9ff2aa884fdc.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
![image](https://user-images.githubusercontent.com/92082233/156842619-e0fdaf98-70e4-484c-8ed5-0fd6c6ea62b2.png)
![image](https://user-images.githubusercontent.com/92082233/156842660-ff429300-b283-4518-81f2-0fdff30c66ec.png)


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
![image](https://user-images.githubusercontent.com/92082233/156843852-993cd0a2-a436-4801-abfb-9e65515e0d47.png)
![image](https://user-images.githubusercontent.com/92082233/156843908-5d4ed4ee-5839-491d-a26d-73510b16cc5a.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
![image](https://user-images.githubusercontent.com/92082233/156845131-2b02fbf7-b529-4737-b45f-929448a6cdbd.png)
![image](https://user-images.githubusercontent.com/92082233/156845153-275bd9eb-d093-455f-a2a8-1c59132d5595.png)
![image](https://user-images.githubusercontent.com/92082233/156845662-a1fafa03-18bb-4510-bfb3-d9894623147c.png)


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###
![image](https://user-images.githubusercontent.com/92082233/156846193-9073ba59-6f4c-4cdd-8c7e-2d6238a8722a.png)


---
