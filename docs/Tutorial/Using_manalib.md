# การใช้งาน Mana Library

    Using manawallib library
        Installation
            html 
                - npm install manawallib
                <head>
                    ...
                    <script src="node_modules/manawallib/dist/bundle.js"></script>
                    ...
                </head>
            ionic
                - npm install manawallib-ion
                - app.module.ts => 
                    import { IonManaLib } from 'manawallib-ion';
                    ...
                    @NgModule({
                      providers: [
                        ...
                        IonManaLib.SetConfiguration("svcid","key"),
                        ...
                      ],
                    })
        Basic usage
            html
            <body>
                <script>
                    $(document).ready(async function () {
                        svc = await manawallib.GetLib();
                        svc.initPageApi(mcontentId, () => {});
                    });
                </script>
            </body>
            ionic
                constructor(private svc: IonManaLib) { }
                this.svc.initPageApi(this.mcontentid); >> ใช้งานขั้นพื้นฐาน initPage(ตั้งค่าเพจ ตั้งค่าให้เรียบร้อยก่อนเรียกใช้งานของมานะ)
		ex=>shopping-cart-pay.page, ppay-payment-creating.page
