# RegisterLoginFlow

 ResgisterLoginFlow APIs call to make mana and 3rd to work together. Mana will send LoginFlowId value for developer to configure config in service created by developer.

## Remove LoginFlowId value

 1.Go to Web Devportal and login

 2.Navigate to APIs and go to the Service Management category.

 3.Click on APIs post ResgisterLoginFlow and press Try it.
 
 4.Take the ServiceId value obtained from the creation of Services and put it in the value of serviceId.

Enter the value Body as a condition of the Service that allows User Mana to login to use. Example
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

Fill in all the information and press Send to get the LoginFlowId value.

 ## Login 3rd using User Mana Login 

 1.There is a web Login page for User Mana to use to login.

 2.User Mana, press Login. In case the identity is not verified, mana will send a QR code for the user to scan the Login instead.

 3.User Mana uses App mana to scan QR, will call API IDP (Rename API) by sending ServiceId and LoginFlowId to check if that User Mana has the right to login according to the 3rd condition set or not. not

 - Scan the QR and meet the conditions that the 3rd set, will be able to see the service that the 3rd created as shown in the picture.

 ![a]( ../img/Tutorial/RegisterLoginFlow/shop.PNG )

 - Scan QR and does not meet the conditions that the 3rd set, will not show the service created by the 3rd as shown in the picture.


 ![a]( ../img/Tutorial/RegisterLoginFlow/noshop.PNG )




