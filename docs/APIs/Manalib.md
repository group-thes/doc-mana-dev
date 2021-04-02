# Manawallib
## Call API
             Call API to Registered URL
                Getapidata
                getApiDataWithEndpointId
             Call Api to external
                CallApiGet ex:eslip-select
                CallApiPost
                CallApiDelete

## Form

### SubmitFormData
  กรอกข้อมูลครบแล้วกดส่งข้อมูลได้


## Title
### SetTitle
              ionic
                <ion-header>
                  <ion-toolbar>
                    <ion-title>{YOUR_TITLE}</ion-title>
                  </ion-toolbar>
                </ion-header>


                html
                <title>{YOUR_TITLE}</title>


                initPageApi               
                this.title = it.eslipStub != null ? it.eslipStub.name : this.title;
                this.svc.initPageApi(this.mcontentid);

             
             
### ToolbarAction ขวาบนกดเพื่อสั่งให้ทำอะไร


## GPS
            Get GPS ใช้ gps หัวด้านบนของมานะ
            Set 
                