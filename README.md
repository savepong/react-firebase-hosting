# React on Firebase Hosting

เริ่มจาก ติดตั้ง

### `npm install -g firebase-tools`

จากนั้นก็ทำการ login และ init firebase project

### `firebase login`

ก็จะมี Popup ขึ้นมา เพื่อให้เราทลงชื่อเข้าใช้ด้วย Email และเข้าถึง Firebase Console ได้ ก็กด Allow (หรืออนุญาต) และหน้า Terminal หลังจากเรากดลงชื่อเข้าใช้และ Allow แล้ว ก็จะมี ข้อความบอกใน Terminal ว่า Success

### `firebase init`

ให้เราเลื่อนไปที่ Hosting และกด spacebar เพื่อเลือก (สังเกตปุ่มกลมๆขาวๆ) จากนั้นกด Enter

### `? What do you want to use as your public directory?`

**Note: พิมพ์เป็น build เพราะว่า `yarn build` มันจะ build static ไปที่โฟลเดอร์ build (default กรณีไม่เปลี่ยนคือ public)**

### `? Configure as a single-page app (rewrite all urls to /index.html)? (y/N)`

พิมพ์ n เพื่อไม่ต้องให้มันเขียนทับไฟล์ที่มีอยู่แล้ว

### Deployment

### `firebase deploy`

ในกรณีที่เราไม่ได้เลือก default project จะเกิด error ขึ้น คือ
Error: No project active. Run with --project <projectId> or define an alias by
ให้เราทำการ ระบุ project ด้วย โดยการใช้คำสั่ง

### `firebase use --add`

ตอนนี้เว็บผมก็ Host บน Firebase เรียบร้อยแล้ว โดยใช้ไฟล์ static จากโฟลเดอร์ build นั่นเอง

### `yarn build`

### `firebase deploy`