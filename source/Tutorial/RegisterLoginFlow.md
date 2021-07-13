# RegisterLoginFlow

Calling APIs RegisterLoginFlow will get LoginId for the developer to configure the service that the developer created.


1.Go to devportal and login
2.Navigate to APIs and go to the Service Management category.
3.Click on APIs post ResgisterLoginFlow and press Try it.
5.Take the ServiceId value obtained from the creation of Services and put it in the value of serviceId.

Put a value in the example body.
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

Fill in all the information and press Send to get the LoginId value.

## 3rd Login System 

1.Create a web page for User Login.

2.User press Login and call API IDP(Rename API) by sending ServiceId and LoginId.

3.API IDP(Rename API) Reply URL back and generate as QR or AppLink.

4.Use App mana scan QR





