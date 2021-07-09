# FromSandbox to Production
During the development of a system, a developer is usually given a Sandbox key (Subscriptions key) as a precursor upon completion of the application. Configuration Or setting a BaseURL to connect to the mana APIs, accessing the key can be done by logging in to the DevPortal and viewing it through the Profile menu.

1.Sign in in Devportal and go to Profile menu to apply Key. 

![a](../img/Tutorial/sand2prod/getkey1.png)

2.In the Profile menu, it will show the information of the Key according to the Tier level registered.

![a](../img/Tutorial/sand2prod/getkey2.png)

If developers wish to [ upgrade Tier to Standard or higher ](../Quickstarts/stepUpgrade_tier.md)to request more access to data. Once a Tier is upgraded, more APIs can be used as the Tier Tier is upgraded. This includes the Publish service.

Therefore, the Publish service is a preparation for the transition from the development phase. (Development) to the preparatory phase for the release of the system to the public (Pre-release) according to the [system development cycle](../Introduction/DevelopmentCycle.md) and including preparing to switch from sandbox to production environment

Therefore, in order to connect to the APIs of a production environment, a Production Key is required. To implement the Production Key, you need to call APIs (production subscriptions) in the DevPortal and configure or set a BaseURL to connect. Connect to production environment APIs

call api sample image

And after the development team has already tested the system in the pre-release period. To bring the system to the public There must be a notification for mana to review and prepare to release it to the public via API calls (Service publish).