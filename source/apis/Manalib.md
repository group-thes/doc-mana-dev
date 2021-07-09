# Mana library
คำสั่งหรือความสามารถต่างๆที่มีใน Mana library มีดังต่อไปนี้
## Call API
* Call API to Registered URL   
  * Getapidata    
  * getApiDataWithEndpointId    
* Call Api to external    
  * CallApiGet ex:eslip-select    
  * CallApiPost     
  * CallApiDelete    

## Form 
เป็นรูปแบบของการกรอกข้อมูลเพื่อส่งข้อมูลเข้าไปประมวลผลในฝั่ง Server โดยมี Form ดังต่อไปนี้
* ValidForm : เป็นการตรวจสอบข้อมูลให้เป็นไปตามเงื่อนไขที่กำหนดก่อนที่จะส่งข้อมูลไปประมวลผล
* SubmitFormData : ส่งข้อมูลที่ผ่านการตรวจสอบแล้วไปประมวลผล
* ConfirmForm : เป็นการเปิด Dialog เพื่อยืนยันการทำงานซึ่งจะได้รับ boolean กลับมา
// มี DLG ยืนยันการทำงาน resolve.isConfirm true false
* SubmitFormDataWithEndpointId //อาจจะยังไม่ได้ใช้

```
  public isFirstTime: boolean = true;
  public fg: FormGroup;

  onSave() {


  if (this.isFirstTime) {
    this.isFirstTime = false;
  }
  this.updateValidationFormToClient();

  if (this.fg.valid) {

    let msg = this.fg.get("isAgree").value == "true" ? "ยืนยันข้อตกลง" : "ปฏิเสธข้อตกลง";

    let message = new confirmMessage("",
      "<span style=\"color: Black; \">คุณต้องการ" + msg + "</span>"
    );

    this.svc.confirmForm(message).then(resolve => {
      if (resolve.isConfirm) {
        let isAgree = this.fg.get("isAgree").value;
        this.fg.get("isAgree").setValue(isAgree == "true");
        this.svc.submitFormData(this.mcontentid, this.fg.value);
      }
    });
  }
}

  updateValidationFormToClient() {
    this.svc.validForm(this.isFirstTime || this.fg.valid)
  }
```


* Selectimage //เลือกรูปที่อยู่ในฟอร์ม ex:merchant-profile-image-edit
* OptionDialog //ลิสต์ให้เลือก ex: account-create-bankaccount => account-bank-select
* CustomNumpad // 

```
    ionic
        <ion-label for="customInputAmount">
            <h2>จำนวนที่ต้องการเติม</h2>
        </ion-label>
        <ion-input type="text" id="customInputAmount" customInput="true" ></ion-input>
    html
        <label for="customInputAmount">ทดสอบ</label>
        <input customInput="true" type="text" class="form-control" id="customInputAmount" placeholder="test">
```


## GPS
            Get GPS ใช้ gps หัวด้านบนของมานะ
            Set 

## Title
* SetTitle : การกำหนดหัวเรื่อง/ชื่อหน้า ให้กับหน้าเพจนั้นๆ   
การกำหนดชื่อโดยทั่วๆไป        
```
ionic
  <ion-header>
    <ion-toolbar>
      <ion-title>{YOUR_TITLE}</ion-title>
    </ion-toolbar>
  </ion-header>


  html
  <title>{หล่อมาก}</title>
```
การกำหนดชื่อหน้าจากข้อมูลที่ส่งมา
```
<!DOCTYPE TS>

  public title = "ร้านของคุณ";

  refreshCallBack() {
    let load$ = this.loadData$();
    this.data$ = load$;
    load$.then((it: any) => {
      this.title = it.name != null ? it.name : this.title;
    });
  }
  ```

### ToolbarAction ขวาบนกดเพื่อสั่งให้ทำอะไร

## Navigation
    VisitEndpoint //สั่งให้เปิดตาม url 
    CallTrigger //กดปุ่มเพื่อ call fc. //อาจจะไม่ได้ใช้
## Currency ex:shopping-cart-pay
    getAmount => 1
    getCurrency => THB
    getMonetaryDisplay => 1 THB
## Etc.
    SetButtonVisibility //ทำให้ปุ่มหาย
    SetStateChangedHandler //คำสั่งเมื่อมี stage ต่างๆเข้ามาจะให้หน้านั้นๆทำอะไร ex:ขอพี่พี
    InitPageApiWithCallBack //หากกลับมาหน้านั้นๆจะให้ทำงานอะไรต่อ, พับแอพลง
    /initPage
        