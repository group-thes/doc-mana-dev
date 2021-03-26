@startuml
participant 3rd_App as Foo
participant 3rd_Server as Foo1
participant DevPortal as Foo2

Foo -> Foo1 : ขอข้อมูล User 
Foo1 -> Foo2 : ส่ง User ID
Foo2 -> Foo2 : ประมวลผล
Foo2 --> Foo1 : respond
Foo1 --> Foo : แสดงข้อมูล User
hide footbox
@enduml