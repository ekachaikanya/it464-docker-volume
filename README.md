# 🐳 Docker Fullstack Volume Demo

โปรเจกต์ตัวอย่างการใช้งาน Docker Compose ร่วมกับ **Volumes** ทั้ง 3 รูปแบบ (Named, Bind Mount, Anonymous)

## 🏗️ โครงสร้างระบบ
- **Frontend**: Nginx (Bind Mount) - [Port 8090]
- **Backend**: Node.js Express (Anonymous Volume) - [Port 3000]
- **Database**: PostgreSQL (Named Volume) - [Port 5432]

## 🚀 วิธีเริ่มใช้งาน
1. **เตรียมโฟลเดอร์ Log:**
```bash
mkdir -p backend/logs
```

# 🐳 Docker Fullstack Volume Demo

โปรเจกต์ตัวอย่างการใช้งาน Docker Compose ร่วมกับ **Volumes** ทั้ง 3 รูปแบบ (Named, Bind Mount, Anonymous)

## 🏗️ โครงสร้างระบบ
- **Frontend**: Nginx (Bind Mount) - [Port 8090]
- **Backend**: Node.js Express (Anonymous Volume) - [Port 3000]
- **Database**: PostgreSQL (Named Volume) - [Port 5432]

## 🚀 วิธีเริ่มใช้งาน
1. **เตรียมโฟลเดอร์ Log:**
```bash
mkdir -p backend/logs
```

สั่งรันระบบ:
```bash
docker-compose up -d --build
```

##เข้าใช้งาน:

หน้าเว็บหลัก: http://localhost:8090

เช็ค API: http://localhost:3000

## 📂 รายละเอียด Volume ที่ใช้ในโปรเจกต์
ตามมาตรฐาน [Docker Storage Documentation](https://docs.docker.com):


| ประเภท | การใช้งาน | ตำแหน่ง/คำสั่ง |
| :--- | :--- | :--- |
| **Bind Mount** | แชร์ Code และ Logs ระหว่าง Host กับ Container | `./frontend/html`, `./backend/logs` |
| **Named Volume** | เก็บข้อมูล Database ให้คงอยู่ถาวรแม้ลบ Container | `db-data` (Docker Managed) |
| **Anonymous** | ป้องกัน `node_modules` จากเครื่อง Host ไปทับใน Container | `/app/node_modules` |

---

### 3. วิธีอัปเดตระบบ
หลังจากแก้ไฟล์เสร็จแล้ว ให้รันคำสั่งเทพนี้ครับ:
```bash
docker-compose up -d --build
```

😎 Docker Docs: Compose