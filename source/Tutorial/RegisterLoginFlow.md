# การใช้ APIs [POST] RegisterLoginFlow

การเรียกใช้ APIs RegisterLoginFlow จะได้ค่า LoginId  เพื่อให้ทางนักพัฒนาระบบมาทำการตั้งค่า Config ใน Service ที่ทางนักพัฒนาระบบทำขึ้น   


1.เข้ามาที่ devportal แล้วทำการ Login

3.เข้าใน APIs แล้วไปที่หมวดหมู่ Service Management

4.กดที่ APIs post ResgisterLoginFlow แล้วกด Try it 

5.เอาค่า ServiceId ที่ได้จากตอนสร้าง Services  มาใส่ใน ค่า Value ของ serviceId

ใส่ค่าใน Body ตัวอย่าง
```
{
  "baId": "string",
  "allowUser": true,
  "allowEmployee": true,
  "allowOwner": true,
  "minimumBizAccountTier": "string",
  "bizAccountType": "string",
  "bizAccountLogisticType": "string",
  "signInCallback": "string",
  "signOutCallback": "string",
  "appCallback": "string"
}
```
กรอกข้อมูลครบแล้วกด Send เพื่อเอาค่า LoginId ได้เลย


# ระบบ 3rd Login 

1.สร้างหน้า web เพื่อให้ User Login

2.User กด Login มีการเรียกใช้ API IDP(เปลี่ยนชื่อ API) โดยการส่งค่า ServiceId และ LoginId

3.API IDP(เปลี่ยนชื่อ API) ตอบ URL กลับมาแล้วสร้างเป็น QR หรือ AppLink

4.ใช้ App mana scan QR





