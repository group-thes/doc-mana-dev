# การใช้ APIs [POST] RegisterLoginFlow

การเรียกใช้ APIs RegisterLoginFlow จะได้ค่า LoginId  เพื่อให้ทางนักพัฒนาระบบมาทำการตั้งค่า Config ใน Service ที่ทางนักพัฒนาระบบทำขึ้น   


1.เข้ามาที่ devportal แล้วทำการ Login

3.เข้าใน APIs แล้วไปที่หมวดหมู่ Service Management

4.กดที่ APIs post ResgisterLoginFlow แล้วกด Try it 

5.เอาค่า ServiceId ที่ได้จากตอน[สร้าง Services]()  มาใส่ใน ค่า Value ของ serviceId 

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


# การ Login กับระบบ 3rd 

1.ทำการ Login เข้าสู่ระบบของ Web 3rd

2.Web 3rd ส่ง ServiceId และ LoginId ให้ IDP

3.IDP ส่งเปิด QR Login with mana

4.ใช้ App mana scan QR 

5.ทำการอนุญาตการ consent

6.Web 3rd ทำการ Login สำเร็จ
