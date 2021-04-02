ใน Mana application จะมีฟังก์ชั่นที่อนุญาตให้ 3rd party ทำการ [Register mContent](www.google.com) เพื่อนำหน้าเว็บที่ทาง 3rd party พัฒนามาแสดงใน Mana application ซึ่งหน้าเว็บที่จะนำมาแสดงสามารถเรียกใช้ความสามารถตามที่ **Mana library** เขียนไว้ หากนักพัฒนาต้องการเรียกใช้งานจะมีขั้นตอนดังนี้
## การติดตั้ง Mana Library 
### ติดตั้งใน Html
1.ติดตั้ง Mana Library ผ่าน Command prompt
```
npm install manawallib
```

2.ใส่ Script ใน tag Head ซึ่งแนะนำให้ใช้ jquery ในการทำงานด้วย
```
<!DOCTYPE html>
<head>
    <script src="node_modules/manawallib/dist/bundle.js"></script>
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"></script>
</head>
```
### ติดตั้งใน Ionic (รองรับการใช้การสำหรับ Ionic4)
1.ติดตั้ง Mana Library ผ่าน Command prompt
```
npm install manawallib-ion
```

2.ไฟล์ app.module.ts ใส่ IonManaLib ใน providers
```
<!DOCTYPE TS>
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
* สำหรับการ run locale test สามารถใส่ .SetConfiguration("svcid","key") หลัง IonManaLibเพื่อเรียกดูหน้า UI  
```
import { IonManaLib } from 'manawallib-ion';
...
@NgModule({
    providers: [
        ...
        IonManaLib.SetConfiguration("svcid","key"),
        ...
    ],
})
```


33333333333333333333
```
<!DOCTYPE html>
<html>
    <head>
        <script src="node_modules/manawallib/dist/bundle.js"></script>
        <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"></script>
    </head>
    <body>
        <script>
            var lib;
            $(document).ready(async function () {
                lib = await manawallib.GetLib();
                await lib.initPageApi("2354512");
                var result = await lib.getApiData("2354512");
            });
            function Confirm()
            {
                console.log("xxx");
                // lib.SubmitFormData("2354512",data);
            }
        </script>
    </body>
</html>
```

## ตัวอย่างการเรียกใช้งาน Mana Library
Basic usage

