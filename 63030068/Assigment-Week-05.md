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
classroom o-- Whiteboard
classroom o-- Table
classroom o-- Chair
classroom o-- Student
classroom o-- Teacher
@enduml 
```

![image](https://user-images.githubusercontent.com/50146617/155976072-001ad194-5d1a-4705-a905-ecf56d36593e.png)

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
![image](https://user-images.githubusercontent.com/50146617/155976226-bf619bd2-4109-498b-bba5-06082edc3392.png)

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

![image](https://user-images.githubusercontent.com/50146617/155976459-a1af8b60-4ced-40c6-8f12-f4b84213bc43.png)


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

![image](https://user-images.githubusercontent.com/50146617/155976675-2209bc84-e2b4-40ef-933e-f9c6dd6bcef4.png)

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
![image](https://user-images.githubusercontent.com/50146617/155976780-9c88d4bf-d7b0-4016-89e8-328c2373e327.png)

### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###

``` puml
@startuml 
class Bank_Account{
    - Bank 
    - Name
    - interest
    # debt
    + deposit()
    + withdraw()
}
class Savings_Account{
    + Pay_utility_bills()
}
class Current_Account{
    Fee
    + daily_check()
}
Bank_Account <|-- Savings_Account
Bank_Account <|-- Current_Account
@enduml
```

![image](https://user-images.githubusercontent.com/50146617/155978711-50fc5781-c09b-41b1-9fd2-b80004416804.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
``` puml
@startuml
class employee {
    # salary
    - work
    + take_leave()
}
class manager {
    - position_allowance
    + work_order()
}
employee <|-- manager
@enduml
```
![image](https://user-images.githubusercontent.com/50146617/155979602-379fe83a-9533-4e54-97a4-62cf37102fd3.png)


### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
``` puml
@startuml
class CD_Player_Music{
    - Brand
    - CD_slots
    + Play_Music()
}
class Video_Player_Music{
    - Brand
    + Player_Video()
}
class CD_Player{ }

CD_Player_Music <|-- CD_Player
Video_Player_Music <|-- CD_Player
@enduml
```
![image](https://user-images.githubusercontent.com/50146617/155980579-71904da1-fb9d-45dd-9189-98eae69dcac8.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###


---
