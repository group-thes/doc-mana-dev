## FromSandbox to Production

ในระหว่างการพัฒนาระบบ ทีมนักพัฒนาสามารถทำการเชื่อม API กับทาง mana ได้โดยการนำ Sandbox key มาใช้งาน ซึ่งหากนักพัฒนาได้ทำการทดสอบเป็นที่เรียบร้อยแล้วและต้องการจะนำระบบออกสู่สาธารณะจะต้องเปลี่ยนมาใช้ Production key ที่ได้มาจาก Devportal พร้อมทั้งทำการเปลี่ยน ฺBaseURL หรือทำ Configuration กับระบบของทีมนักพัฒนาเพื่อใช้งานร่วมกันกับ API ของ mana โดยมีขั้นตอนการดังนี้

1.ทำการ Sign in ใน Devportal ให้เรียบร้อย

![a](../img/Tutorial/sand2prod/getkey1.png)

2.ไปที่เมนู Profile เพื่อนำ Key มาใช้ในการทำงาน 

![a](../img/Tutorial/sand2prod/getkey2.png)