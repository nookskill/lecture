# Survival Guide

- ใช้ ```CTRL-SPACE``` เพื่อเรียกดูรายการเสนอแนะและคำสั่งต่างๆ
- อ่านข้อความเออเร่อเพื่อหาสาเหตุ, ไฟล์ และบรรทัดที่เกิดเออเร่อขึ้น
- ตรวจสอบคลาสที่อิมพอร์ตมาว่ามาจากแพคเกจที่ถูกต้องหรือไม่
- ตรวจสอบว่ามีไลบรารี่ครบถูกต้องหรือไม่
- เซิฟเวอร์ต้องมีการรีคอมไพล์ไฟล์หลังแก้ไขในบางกรณี ฉะนั้นควรรอสักพัก หรือรีสตาร์ทเซิฟเวอร์ก่อนเปิดในเว็บบราวเซอร์
- ***เว็บบราวเซอร์ในโปรแกรม Eclipse กากมาก ถ้าเป็นไปได้ควรหลีกเลี่ยง***
- ปิดและเปิดใหม่/ลบและเพิ่มใหม่แก้ได้หลายปัญหา เช่น ปิดและเปิดโปรแกรม Eclipse ใหม่, ลบและเพิ่มเซิฟเวอร์ใหม่
- สร้างโปรเจคใหม่แก้ได้หลายปัญหาเช่นกัน
- รีสตาร์ทเครื่องแก้ได้หลายปัญหาเช่นกัน
- ไฟล์ที่อยู่ในห้อง META-INF และ WEB-INF จะ**ไม่สามารถเข้าถึงได้จากเว็บบราวเซอร์**
- พยายามเปลี่ยนจาก US-ASCII เป็น UTF-8
- อย่าตั้งชื่อตัวแปรมั่ว ตั้งให้คนอื่นรู้เรื่องด้วย
- 500 แค่บอกว่าเกิดข้อผิดพลาดในโค้ดของเรา อยากรู้ว่าเกิดที่ไหนให้ดูข้างล่าง ![](https://pbs.twimg.com/media/BgCHDU8CMAArTiv.png:large)
- ทำไปสั่งปริ้นไป ดูว่าค่าต่างๆ ถูกต้องไหม
- ถ้าขึ้นแบบนี้หมายความว่าอาจจะมีโปรเซส tomcat ค้างอยู่ให้หาทางปิด (terminal (killall java), task manager (javaw.exe), ...) ![](http://i.stack.imgur.com/JNGQK.png)
- ถ้าเจอ ```HTTP Status 500 -  According to TLD or attribute directive in tag file, attribute test does not accept any expressions``` ให้ลองดูบรรทัดบนสุดว่ามี /jsp อยู่หน้า /jstl ไหม
- ใช้ &lt;c:if&gt; หรือ &lt;c:when&gt; แล้วมันไม่ยอมเข้าเงื่อนไข ให้ลองดูว่าในส่วนของ test="" มีเว้นวรรคเกินก่อนปิด double quote หรือไม่ ถ้ามีเกินให้ลบออก
- อย่าลืมกด Apply หลังเปลี่ยนแปลงค่าแล้วใน MySQL Workbench
- หากเจอ Error ![](http://i.imgur.com/093IDfO.jpg)  ให้ copy ตัว jstl-api-1.2.jar กับ  jstl-impl-1.2.jar ไปใส่ใน WEB-INF/libs
- หากต้องการรับ input ภาษาไทย ต้องใส่ ```<meta charset="utf-8">``` ใน html และใส่ ```request.setCharacterEncoding("UTF-8");``` ก่อนรับค่าทุกครั้ง see more [1](http://stackoverflow.com/questions/11002827/html-forms-and-jsp-problems-with-utf-8-character-encoding) [2](http://stackoverflow.com/questions/12968472/how-to-solve-utf-8-in-java)
