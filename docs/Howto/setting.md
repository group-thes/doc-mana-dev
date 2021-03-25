
## Setting Key 
ในระหว่างการพัฒนาระบบ โดยปกติแล้วเมื่อทำการสมัครเป็นนักพัฒนาเรียบร้อยแล้วจะได้รับ Sandbox key เป็นตัวตั้งต้นซึ่งสามารถนำ key ที่ได้รับไปใช้ในระบบของทีมนักพัฒนาไม่ว่าจะเป็นการทำ Configuration หรือการเปลี่ยน ฺBaseURL เพื่อทำการเชื่อมต่อกับ API ของ mana 

ซึ่งหากนักพัฒนามี[การสมัครหรือเปลี่ยนแปลงเป็น tier ที่สูงขึ้น](../Quickstarts/stepUpgrade_tier.md) จะได้รับ Production Key เพิ่มขึ้นเพื่อสามารถเข้าสู่ API ที่หลากหลายขึ้นซึ่งรวมถึงการ Publish service to production โดยการเข้าถึง Key นั้นสามารถทำได้ผ่านการ Login เข้าสู่ DevPortal และดึงข้อมูลผ่าน API ที่กำหนด

![a](../img/Quickstarts/settingKey/settingKey.PNG)

ซึ่งหากเป็นดังภาพด้านบนทางทีมงานของ mana มีข้อแนะนำให้นักพัฒนาทำการสร้าง app ที่แยกการพัฒนากับตัวที่ปล่อยจริงออกจากกันเพื่อให้ง่ายต่อการ

![a](../img/Quickstarts/settingKey/settingKey2.PNG)


<!-- ซึ่งนอกจากการเปลี่ยน Key แล้วในการทำงานภายใต้ Environment ที่แตกต่างกันอาจรวมถึงการเปลี่ยน ฺBaseURL จาก Sandbox เป็น Production  -->

<!-- ## การตั้งค่าการใช้งานใน Mana Production
เมื่อนักพัฒนาต้องการจะแก้ไขหรือเปลี่ยนแปลง Application Server หรือทำ Configuration ของทีมนักพัฒนาให้สามารถใช้งานกับ Mana production ต้องนำ Production-Key ที่ได้มาจาก DevPortal ไปแก้ไขในระบบของนักพัฒนา ซึ่งรวมถึงการเปลี่ยน ฺBaseURL จาก Sandbox เป็น Production  -->
