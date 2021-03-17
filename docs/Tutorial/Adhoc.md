# Using Adhoc Service
เป็นบริการการสร้าง QR เพื่อจ่ายเงินให้กับร้านค้าชนิดหนึ่ง ซึ่งผู้ใช้งานไม่จำเป็นต้องกรอกข้อมูลหรือรายเอียดใดๆเพิ่มเติม สามารถใช้งานได้โดยการแสกน QR ผ่านทางแอพพลิเคชั่นใดๆก็ตามเพื่อทำการจ่ายเงินให้กับร้าน โดยหากนักพัฒนาต้องการใช้บริการสามารถทำได้ตามขั้นตอนด้านล่างดังนี้

1. ทำการสร้าง [Software Ba](https://google.com) ใน Mana Application 
2. สร้าง Service ที่ API-Management ซึ่งในขั้นตอนนี้จะได้ ServiceId เพื่อเอาไว้ใช้งาน
3. นำ ServiceId ที่ได้มาทำการ Register AdhocPaymentHook ที่ API-Management 
4. ทดสอบการทำงานโดยทำการทดสอบผ่าน Mana Sandbox Application
5. หากต้องการจำลองหรือทดสอบระบบในสภาวะแวดล้อมจริงสามารถใช้งานได้ผ่าน [Production environments](https://google.com)

### สามารถลองใช้งาน Adhoc Service ผ่านทาง [API-Management](https://google.com)
