# RegisterLoginFlow
 
การเรียกใช้ APIs ResgisterLoginFlow เพื่อให้ mana กับ 3rd สามารถทำงานร่วมกันได้ โดย mana จะส่งค่า LoginFlowId  เพื่อให้ทางนักพัฒนาระบบมาทำการตั้งค่า Config ใน Service ที่ทางนักพัฒนาระบบทำขึ้น  

## ขั้นตอนการรับค่า LoginFlowId

1.เข้า Web Devportal แล้วทำการ Login

2.เลือกเมนู APIs แล้วเลือกหมวด Service Management

3.เลือก APIs post ResgisterLoginFlow แล้วกด Try it

4.นำค่า ServiceId ที่ได้จากตอน[สร้าง Services](../Tutorial/CreateServices.md)  มาใส่ใน Value ของ serviceId

5.กำหนดค่าใน Body ที่จะใช้เป็นเงื่อนไขของ Service เพื่อที่จะสามารถ Login เข้าใช้งานได้

เมื่อกรอกข้อมูลครบแล้วกด Send จะได้รับค่า LoginFlowId 

 ตัวอย่าง Body ที่จะให้ User Mana ทั้งหมด สามารถ login ใช้งาน Service
```
{
  "baId": "string",
  "allowUser": true,
  "allowEmployee": false,
  "allowOwner": false,
  "minimumBizAccountTier": "string",
  "bizAccountType": "string",
  "bizAccountLogisticType": "string",
  "signInCallback": "string",
  "signOutCallback": "string",
  "appCallback": "string"
}
```

 ตัวอย่าง Body ที่จะให้ User Mana ที่เป็นพนักงานอย่างเดียว สามารถ login ใช้งาน Service
```
{
  "baId": null,
  "allowUser": false,
  "allowEmployee": true,
  "allowOwner": false,
  "minimumBizAccountTier": "string",
  "bizAccountType": "string",
  "bizAccountLogisticType": "string",
  "signInCallback": "string",
  "signOutCallback": "string",
  "appCallback": "string"
}
```

 ตัวอย่าง Body ที่จะให้ User Mana ที่เป็นพนักงานและเจ้าของ สามารถ login ใช้งาน Service
```
{
  "baId": null,
  "allowUser": false,
  "allowEmployee": false,
  "allowOwner": true,
  "minimumBizAccountTier": "string",
  "bizAccountType": "string",
  "bizAccountLogisticType": "string",
  "signInCallback": "string",
  "signOutCallback": "string",
  "appCallback": "string"
}
```

## Login 3rd โดยใช้ User Mana Login 

1.มีหน้า web Login เพื่อให้ User Mana ใช้ Login

2.User Mana กด Login 3rd จะมีการใช้ API IDP(เปลี่ยนชื่อ API) โดยจะส่งค่า ServiceId และ LoginFlowId เพื่อให้ IDP เช็คว่า User Mana คนนั้นมีสิทธิ์ Login เข้าใช้งานตามเงื่อนไขที่ 3rd กำหนดไว้ได้หรือไม่

3.IDP ตรวจสอบข้อมูลเสร็จจะส่ง response กลับให้ 3rd 


  - 3.1 กรณีที่ IDP check แล้วเงื่อนไขผ่าน IDP จะส่ง baid และ ค่า Extra ให้กับ 3rd 

ค่า Extra ที่ IDP ส่งมาให้ 3rd
```
{
    Id  // รหัสข้อมูลผู้ใช้
    DisplayName  // ชื่อข้อมูลผู้ใช้
    PictureUrl   // รูป profile เป็น url
    ExProperties
        {
          loginas         // ทำการ login เข้าใช้งานในฐานะอะไร User, Employee, Owner, CoOwner
          refid           // รหัสพนักงานที่ register มา
          jobtitle        // ตำแหน่งพนักงานที่เขา register มา
          baid            // รหัสของร้านที่ user เลือก 
          serviceid       // รหัส service ที่ RegisterLoginFlow
          basubscribed    // ร้านได้ใช้ Service นี้หรือเปล่า?
        }
}
```
ข้อมูลที่ IDP ส่งมา 3rd สามารถนำข้อมูลนั้นมาเช็คเงื่อนไขในการ login เพิ่มได้ ยกตัวอย่างเช่น พนักงานเฉพาะตำแหน่งผู้จัดการถึงจะสามารถ login services นี้ได้ ฯลฯ

  - 3.2 กรณีที่ IDP check แล้วเงื่อนไขไม่ผ่าน User Mana จะไม่สามารถ Login เข้าใช้งาน service ได้

<!-- 2.User Mana กด Login ซึ่งในกรณีที่ยังไม่ยืนยันตัวตน  mana จะส่ง QR มาเพื่อให้ User สแกน Login เข้าไปแทน

- สแกน QR แล้วตรงตามเงื่อนไขที่ตรงตามที่ 3rd กำหนดจะสามารถเห็น Service ที่ 3rd สร้างขึ้นมาดังรูป  

![a](../img/Tutorial/RegisterLoginFlow/shop.PNG)


- สแกน QR แล้วไม่ตรงตามเงื่อนไขที่ตรงตามที่ 3rd กำหนดจะไม่ขึ้น Service ที่ 3rd สร้างขึ้น ดังรูป  


![a](../img/Tutorial/RegisterLoginFlow/noshop.PNG) -->



