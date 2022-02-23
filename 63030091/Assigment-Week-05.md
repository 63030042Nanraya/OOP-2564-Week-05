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

![image](https://user-images.githubusercontent.com/92081884/155303736-e62a449f-8292-40d5-b4ef-a1abc0b93c66.png)

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

![image](https://user-images.githubusercontent.com/92081884/155303912-f4a7c489-cc96-461b-9c5e-3e0a1df42cb0.png)

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

![image](https://user-images.githubusercontent.com/92081884/155304008-fd62631f-dfaa-4c53-98c7-51c367fccffa.png)

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

![image](https://user-images.githubusercontent.com/92081884/155308632-8aa5eb72-840f-4f12-a855-af0d986a9119.png)

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

MotorBoat o-- Helm
MotorBoat o-- Engine

Car o-- Engine
Car o-- Door
Car o-- Wheel
Car o-- SteeringWheel
@enduml 
```

![image](https://user-images.githubusercontent.com/92081884/155308731-4355a239-ce4c-429b-8fd8-4b78d5cb05ad.png)

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

![image](https://user-images.githubusercontent.com/92081884/155308825-b84238dd-2909-4499-a537-5704af7c46e8.png)

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
class Index{}
class Content{}
class Bibliography{}

Book o-- "2..2" Cover
Book o-- "1..1" Introduction
Book o-- "1..1" Index
Book o-- "1..N" Content
Book o-- "1..1" Bibliography
@enduml 
```

![image](https://user-images.githubusercontent.com/92081884/155308964-04c552be-306a-465e-a883-77f52a39eb51.png)

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
```

![image](https://user-images.githubusercontent.com/92081884/155309249-fe7bf951-254e-46cf-b2e5-16b0bacca330.png)

### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###

![image](https://user-images.githubusercontent.com/92081884/155305380-1cad681b-f4fc-4fa0-8b44-f8d1d91a2d74.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###

![image](https://user-images.githubusercontent.com/92081884/155305496-7027984c-b1af-440c-8cf4-395e6a49fae0.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###

![image](https://user-images.githubusercontent.com/92081884/155305570-9accf33f-60ed-4958-aa17-1c56919220f9.png)
![image](https://user-images.githubusercontent.com/92081884/155305656-e68cf1f6-cd8f-47a3-ba23-dcc1e6bdc770.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###

![image](https://user-images.githubusercontent.com/92081884/155305766-67064e7c-8e5f-4baa-b4d3-e2a1e1aa27ea.png)

---
