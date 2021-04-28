# API Products
Features ต่างๆที่ทาง mana เปิดให้นักพัฒนาสามารถเข้าใช้งานผ่าน API โดยแบ่งแยกออกตามหมวดหมู่ได้ดังนี้
## [Service Management](https://mana-sand-portal.developer.azure-api.net/api-details#api=dev-master-service-management "Link To sandbox")
การบริการว่าด้วยเรื่องของการสร้างตัวตนและกำกับดูแลให้สามารถเรียกใช้งานข้อมูลที่ได้ลงทะเบียนไว้ได้ เช่นการลงทะเบียนเพื่อเปิดใช้งานระบบ การส่งข้อมูลจากผู้ให้บริการเมื่อเกิดเหตุการณ์บางอย่างในขณะนั้น การแสดงหน้าเว็บของนักพัฒนาบน Mana application เป็นต้น API ในหมวด Service Management ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* Services
* Hook
* mContent
```

## [Service Publishing](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การจัดการบริการเกี่ยวกับการเตรียมข้อมูลให้พร้อมในการใช้งานสำหรับ Production environment เช่น การนำ Service เผยแพร่สู่ตลาด API ในหมวด Service Publishing ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* Publish services
```
 
## [Business Management](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การจัดการบริการด้านธุรกิจ ไม่ว่าจะเป็นเรื่องของควบคุมดูแลธุรกิจต่างๆ ทั้งการจัดการเรื่องการเงินและพนักงาน เช่น การสร้างร้านค้า การสมัครเป็นพนักงานในร้าน เป็นต้น API ในหมวด Business Management ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* BA
* Employee
```

## [Membership Management](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การจัดการเกี่ยวกับระบบสมาชิกที่คุณสามารถจัดการให้สิทธิประโยชน์กับผู้ใช้งานที่เป็นสมาชิกของร้านคุณ เช่น การจ่ายเงินร้านค้าถึงจำนวนที่กำหนดสมาชิกจะได้รับแต้มเพื่อนำไปใช้แลกของรางวัล เป็นต้น

## [Products and Orders](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การบริการการจัดเก็บข้อมูลสินค้าของร้านค้า รวมถึงการเก็บข้อมูลต่างๆของสินค้าทุกชิ้นที่ถูกเลือกไว้ในตะกร้า เช่น การเก็บข้อมูลสินค้าที่ร้านค้าทำการสร้าง การเก็บข้อมูลสินค้าที่ถูกเลือกไว้ในตะกร้า เป็นต้น

## [Promotions](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
<!-- บริการด้านโปรโมชั่น ทั้งการสร้างโปรโมชั่น จัดการและดูผลสรุปของของโปรโมชั่นของคุณได้ ทาง mana เปิด api ไว้ให้ 3rd เพื่อใช้ในทดสอบ เช่น การสร้างโปรโมชั่น, การใช้โปรโมชั่นเพื่อให้ได้รับส่วนลด เป็นต้น API ในหมวด Promotions ที่ทาง mana จัดเต็มไว้ให้ มีดังนี้ -->
การบริการการส่งเสริมการตลาด เช่นการสร้างโปรโมชั่นเพื่อให้ลูกค้าได้รับสิทธิประโยชน์ผ่านการใช้งานคูปอง เป็นต้น API ในหมวด Promotions ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* ESlip
```

## [Transaction Management](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การจัดการบริการสำหรับธุรกรรมทุกประเภทไม่ว่าจะเป็นเรื่องการเงิน การซื้อขาย การทำสัญญา เช่น การสร้างสัญญาในการดำเนินธุรกิจ การขอความยินยอมในเรื่องต่างๆ เป็นต้น API ในหมวด Transaction Management ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* Escrow
* Budget
* Allowance
* Contract
* Consent
```

## [Interaction and Messaging](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
<!-- การบริการด้านการติดต่อสื่อสารไปรวมถึงการแจ้งเตือนการอัพเดทข้อมูลต่างๆ ไปยังสมัครสมาชิกที่ติต่อกับร้านค้าของท่าน ทาง mana เปิด API ไว้ให้ 3rd เพื่อใช้ในทดสอบ เช่น การแจ้งเตือนการเติมเงิน ถอนเงิน เป็นต้น API ในหมวด Interaction and Messaging ที่ทาง mana จัดเต็มไว้ให้ มีดังนี้ -->
การบริการที่ก่อให้เกิดปฏิสัมพันธ์ระหว่างผู้ให้บริการกับผู้ใช้บริการ การแจ้งเตือน การอัพเดทข้อมูล เช่น การแจ้งเตือนการเติมเงิน-ถอนเงิน การยืนยันข้อมูล การสแกน QR เป็นต้น 
API ในหมวด Interaction and Messaging ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* Feed
* QR
```

## [Data Analytics](https://mana-sand-portal.developer.azure-api.net/apis "Link To sandbox")
การบริการเกี่ยวกับการวิเคราะห์ข้อมูลเพื่อให้การทำธุรกิจของคุณสามารถดำเนินไปได้ตามวัตถุประสงค์โดยมีข้อมูลประกอบการวิเคราะห์และตัดสินใจ เช่น ลูกค้าให้คะแนนความพึงพอใจหลังการใช้บริการ เป็นต้น API ในหมวด Data Analytics ที่ทาง mana จัดเตรียมไว้ให้มีดังนี้
```
* Rating
```