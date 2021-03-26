
## FromSandbox to Production

ในระหว่างการพัฒนาระบบทีมนักพัฒนาสามารถทำการเชื่อม API กับทาง mana ได้โดยการนำ Sandbox key มาใช้งาน ซึ่งหากนักพัฒนาได้ทำการทดสอบเป็นที่เรียบร้อยแล้วและต้องการจะนำระบบออกสู่สาธารณะจะต้องทำการ Publicsh service ซึ่งต้องใช้ Production key ที่ได้มาจาก Devportal ในการทำงานพร้อมทั้งทำการเปลี่ยน ฺBaseURL หรือทำ Configuration กับระบบของทีมนักพัฒนาเพื่อใช้งานร่วมกันกับ API ของ mana

![a](../img/Quickstarts/settingKey/settingKey.PNG)

ซึ่งหากเป็นดังภาพด้านบนทางทีมงานของ mana มีข้อแนะนำให้นักพัฒนาทำการสร้าง app ที่แยกการพัฒนากับตัวที่ปล่อยจริงออกจากกันเพื่อให้ง่ายต่อการ

![a](../img/Quickstarts/settingKey/settingKey2.PNG)


<!-- ซึ่งนอกจากการเปลี่ยน Key แล้วในการทำงานภายใต้ Environment ที่แตกต่างกันอาจรวมถึงการเปลี่ยน ฺBaseURL จาก Sandbox เป็น Production  -->

<!-- ## การตั้งค่าการใช้งานใน Mana Production
เมื่อนักพัฒนาต้องการจะแก้ไขหรือเปลี่ยนแปลง Application Server หรือทำ Configuration ของทีมนักพัฒนาให้สามารถใช้งานกับ Mana production ต้องนำ Production-Key ที่ได้มาจาก DevPortal ไปแก้ไขในระบบของนักพัฒนา ซึ่งรวมถึงการเปลี่ยน ฺBaseURL จาก Sandbox เป็น Production  -->
