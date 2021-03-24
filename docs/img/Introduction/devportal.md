@startuml
participant 3rd_App as Foo
participant 3rd_Server as Foo1
participant DevPortal as Foo2
participant Mana_Server as Foo3



Foo -> Foo1 : ขอข้อมูล User 
Foo1 -> Foo2 : ส่ง User ID
Foo2 -> Foo3 : ส่ง User ID
Foo3 -> Foo3 : ประมวลผลทำการค้นหา\nUser ID
Foo3 --> Foo2 : respond
Foo2 --> Foo1 : respond
Foo1 --> Foo : แสดงข้อมูล User


@enduml