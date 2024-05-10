# API คืออะไร ?
API ย่อมาจาก Application Programming Interface เป็นช่องทางในการเชื่อมต่อเพื่อแลกเปลี่ยนข้อมูลกันระหว่างแอพพลิเคชั่น โดยการใช้งานจะแบ่งออกเป็น 3 รูปแบบ
![P1](https://miro.medium.com/v2/resize:fit:720/format:webp/1*DGUIIe8k1vUnC28aL5mNeA.png) 

### - Private API หมายถึง API ที่ใช้งานเพื่อเชื่อมต่อกันระหว่างแอพพลิเคชั่นภายในองค์กรเท่านั้น ไม่สามารถเรียกใช้งานภายนอกองค์กรได้

### - Partner API หมายถึง API ที่เปิดให้ใช้งานเฉพาะ Partner หรือ คู่ค้าทางธุรกิจ ซึ่งจะจำกัดช่องทางในการเชื่อมต่อ API ไว้และเปิดให้ใช้งานเฉพาะ Partner ที่ทำข้อตกลงการใช้บริการเท่านั้น

### - Public API หมายถึง API ที่เปิดให้บริการแบบสาธารณะ ซึ่งจะเปิดให้ผู้พัฒนาแอพพลิเคชั่นอื่นๆ สามารถใช้งานได้เลย โดยส่วนใหญ่จะเป็น API ที่สามารถเรียกใช้งานได้ฟรีหรือเรียกใช้งานได้จำกัดจำนวน ซึ่งถ้าหากต้องการเรียกใช้งานแบบไม่จำกัดจำนวนอาจจะมีการคิดค่าบริการหรือทำข้อตกลงการใช้งานในรูปแบบ Partner API แทน

### การพัฒนา API ที่ได้รับความนิยมในปัจจุบัน
จะพัฒนาโดยทำงานในรูปแบบที่เรียกว่า “ REST API ”(RESTful web services)
![P2](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*u-dukpgFbp51zgq3QsKLEg.jpeg) 




# REST (Representational State Transfer) 
### API คือการสร้าง API ประเภท RESTful web services ซึ่งจัดเป็น Web Service รูปแบบหนึ่งที่ทำงานอยู่บนพื้นฐานของโปรโตคอล HTTP และ HTTPS ประกอบด้วย Request และ Response ตามรูปแบบของ HTTP ที่รับส่งข้อมูลหรือเนื้อหาในรูปแบบของ XML , SOAP , JSON

![P3](https://miro.medium.com/v2/resize:fit:720/format:webp/1*2QF3FeeBQjr39-enEHYHKQ.png) 

## REST API 
### ทำงานโดยใช้พื้นฐานของโปรโตคอล HTTP ดังนั้นแต่ละ Method ของ HTTP จึงนำมาใช้งานใน REST API โดยนักพัฒนา API จะเขียนโปรแกรมให้ API นั้นประมวลผลกับข้อมูลตามความหมายของ HTTP Method

#### - GET หมายถึง ดึงข้อมูล
#### - POST หมายถึง สร้างข้อมูลใหม่
#### - PUT หมายถึง การแก้ไขข้อมูลทั้งหมด
#### - PATCH หมายถึง การแก้ไขข้อมูลบางส่วน
#### - DELETE หมายถึง ลบข้อมูล

## HTTP Status Code 
### คือ รหัสที่บ่งบอกสถานะการทำงานของ Request

#### - 200 (OK) — ดำเนินการเสร็จสมบูรณ์ไม่มีข้อผิดพลาด
#### - 201 (Created) — สร้างข้อมูลหรือ Resource ใหม่เสร็จสมบูรณ์ไม่มีข้อผิดพลาด
#### - 202 (Accepted) — ได้รับ Request แล้วและกำลังประมวลผลข้อมูล แต่ยังประมวลผลไม่เสร็จสมบูรณ์
#### - 204 (No Content) — ได้รับข้อมูลจาก request แล้วแต่จะไม่มีข้อมูลใดๆกำหนดในส่วนของ Body และ Response
#### - 400 (Bad Request) — ส่ง Request หรือข้อมูลผิดรูปแบบ
#### - 401 (Unauthorized )— ไม่มีสิทธิ์เรียกใช้งาน API สาเหตุเกิดจากไม่ได้ส่ง HTTP Header ที่ชื่อ WWW-Authenticate มาด้วย หรือ ส่ง WWW-Authenticate (username,password , token) มาแล้วไม่มีสิทธิ์ใช้งาน
#### - 403 (Forbidden) — Client ไม่มีสิทธิ์ใช้งาน API นี้โดยเฉพาะ
#### - 404 (Not Found ) — ไม่พบ URL , API ที่เรียกใช้งาน
#### - 405 (Method Not Allowed) — API ไม่รองรับ Method ที่ระบุใน Request
#### - 500 (Internal Server Error) — เกิดข้อผิดพลาดที่ฝั่ง Server

