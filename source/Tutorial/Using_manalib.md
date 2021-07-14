# Client library
ใน Mana application มีความสามารถให้ 3rd party ทำการ [Register mContent](www.google.com) เพื่อนำหน้าเว็บที่ทาง 3rd party พัฒนามาแสดงใน Mana application ซึ่งหน้าเว็บที่จะนำมาแสดงสามารถเรียกใช้ความสามารถตามที่ [Client library](../APIs/Manalib.md) ระบุไว้โดยมีวิธีการติดตั้งและเรียกใช้งานดังนี้
## การติดตั้งและเรียกใช้งาน Client Library ใน Html
### วิธีการติดตั้ง
1.ติดตั้ง Client Library ผ่าน Command prompt
```
npm install manawallib
```

2.ใส่ Script ใน tag Head ซึ่งแนะนำให้ใช้ jquery ในการทำงานด้วย
```html
<head>
    <script src="node_modules/manawallib/dist/bundle.js"></script>
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"></script>
</head>
```
### ตัวอย่างการใช้งาน
การเรียกใช้งานคำสั่งต่างๆใน Client Library ทาง mana แนะนำให้เรียกใช้งานคำสั่ง .initPageApi เป็นอันดับแรก เพื่อเป็นการแจ้งหน้าที่จะใช้งานให้กับ Server เพื่อที่จะได้เตรียมข้อมูลมาแสดงได้อย่างถูกต้อง หลังจากนั้นจึงเรียกใช้งานคำสั่งอื่นๆในลำดับต่อไป    
```html
<html>
    <head>
        ....
    </head>
    <body>
        <script>
            var lib;
            $(document).ready(async function () {
                lib = await manawallib.GetLib();
                await lib.initPageApi("mcontentId");
                var result = await lib.getApiData("mcontentId");
            });
            function Confirm()
            {
                lib.SubmitFormData("mcontentId",data);
            }
        </script>
    </body>
</html>
```
## การติดตั้งและเรียกใช้งาน Client Library ใน Ionic (รองรับการทำงานสำหรับ Ionic4)
### วิธีการติดตั้ง
1.ติดตั้ง Client Library ผ่าน Command prompt
```
npm install manawallib-ion
```

2.ไฟล์ app.module.ts ใส่ IonManaLib ใน providers
```typescript
import { IonManaLib } from 'manawallib-ion';
...
@NgModule({
    providers: [
        ...
        IonManaLib,
        ...
    ],
})
```
* สำหรับการ Run locale test สามารถใส่ .SetConfiguration("svcid" ,"key") หลัง IonManaLib เพื่อแสดงหน้าตา UI  
```typescript
import { IonManaLib } from 'manawallib-ion';
...
@NgModule({
    providers: [
        ...
        IonManaLib.SetConfiguration("svcid" ,"key"),
        ...
    ],
})
```
### ตัวอย่างการใช้งาน
การเรียกใช้งานคำสั่งต่างๆใน Client Library ทาง mana แนะนำให้เรียกใช้งานคำสั่ง .initPageApi เป็นอันดับแรก เพื่อเป็นการแจ้งหน้าที่จะใช้งานให้กับ Server เพื่อที่จะได้เตรียมข้อมูลมาแสดงได้อย่างถูกต้อง หลังจากนั้นจึงเรียกใช้งานคำสั่งอื่นๆในลำดับต่อไป 
```typescript

import { IonManaLib } from 'ion-m-lib';

public mcontentid = "user-profile";
constructor(private svc: IonManaLib) { }

private loadData$() {
    return this.svc.initPageApi(this.mcontentid).then(() => {
    return this.svc.getApiData(this.mcontentid);})
}

onSave() {
    if (this.fg.valid) {
        this.svc.submitFormData(this.mcontentid, this.fg.value);}
}
```