@startuml
participant Mana_App as Foo
participant Mana_Server as Foo1
participant 3rd_Server as Foo2

Foo -> Foo1 : กดสั่งซื้อสินค้า 
Foo1 -> Foo2 : <hook> ถามมีสินค้าไหม ?
Foo2 -> Foo2 : ประมวลผล
Foo2 --> Foo1 : respond
Foo1 --> Foo : แสดงข้อมูล respond

@enduml