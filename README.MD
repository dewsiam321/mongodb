# API ตรวจหวยด้วย NodeJS +  MongoDB

ทำ WebScarab จากเว็บไซต์ [กระปุกดอทคอม](http://lottery.kapook.com/history.html) แล้วทำการบันทึกข้อมูลลงฐานข้อมูล (MongoDB) ด้วย NodeJS
สรุปรวม demo code
  - ทำการร้องขอการเชื่อมต่อ HHTP (HTTP requests) ผ่านโมดูล [request](https://www.npmjs.com/package/request)
  - ทำการแปลง tag html โดยใช้ [cheerio](https://github.com/cheeriojs/cheerio)
  - บันทึกข้อมูลที่ได้ลงฐานข้อมูลของ [MongoDB](https://www.mongodb.com/)
  - เปิดเว็บเซิฟเวอร์และทำการ Routing ผ่าน [express](https://www.npmjs.com/package/express) โมดูล

### เริ่มต้นใช้งาน
1. ติดตั้ง [NodeJS](https://nodejs.org/en/) จากนั้นทำการตรวจสอบว่า Node สามารถใช้งานได้และมี npm สำหรับลงโมดูลเสริมต่างๆหรือไม่โดยใช้คำสั่ง
```sh
$> node --version
 v6.11.4
$> npm --version
 v3.10.10
```
2. ติดตั้ง [MongoDB](https://www.mongodb.com/) จากนั้น set path แล้วตรวจสอบว่า MongoDB ที่ติดตั้งสามารถใช้งานได้หรือยัง โดยใช้คำสั่ง
```sh
$> mongod
```
3. ลองเชื่อมต่อฐานข้อมูลโดยใช้คำสั่ง 
```sh
$> mongo
```
4. clone project (https://github.com/winaibuttasart/LotteryWithMongoDB) จากนั้น run ไฟล์ scrap.js ข้อมูลจะถูกเก็บไว้ที่ document lottery
```sh
$> git clone https://github.com/winaibuttasart/LotteryWithMongoDB.git
$> cd LotteryWithMongoDB
LotteryWithMongoDB/ $> node scrap.js
```

5. run ไฟล์ server.js เพื่อดู API จากการดึงข้อมูลจาก MongoDB มาแสดง
```sh
LotteryWithMongoDB/ $> node server.js
 node run at http://localhost:8080
```
- Get method  http://localhost:8080/{year}/{month}/{date}
- Post method http://localhost:8080/

** แนะนำการตรวจสอบการทำงานของ Post method ผ่าน [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=th)

----
Code by NIZE
----
**More on github**
github https://github.com/winaibuttasart