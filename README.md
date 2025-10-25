# FM2026 Thai Language Pack

สำหรับการแปล Football Manager 2026 เป็นภาษาไทย 
---

## 📋 ข้อกำหนดเบื้องต้น

- Git
- Terminal/Command Prompt

---

## 🚀 วิธีการตั้งค่า

### macOS

#### ขั้นตอนที่ 1: ไปยังไดเรกทอรี่โครงการ

```bash
cd /Users/YOUR_USERNAME/Public/Sports\ Interactive/Football\ Manager\ 26/languages
```

> **หมายเหตุ**: แทนที่ `YOUR_USERNAME` ด้วยชื่อผู้ใช้ Mac ของคุณ

#### ขั้นตอนที่ 2: Clone Repository

```bash
git clone https://github.com/ingpawat/fm2026_thai_opensource.git
cd fm2026_thai_opensource
```

#### ขั้นตอนที่ 3: แตกไฟล์ .gz

```bash
# แตกไฟล์ compressed
gunzip *.gz

# ตรวจสอบไฟล์ที่แตกออกมา
ls -la *.ltf *.ltc
```


---

### Windows

#### ขั้นตอนที่ 1: เปิด Command Prompt หรือ PowerShell

กด `Win + R` พิมพ์ `cmd` และกด Enter

#### ขั้นตอนที่ 2: ไปยังไดเรกทอรี่โครงการ

```cmd
cd C:\Users\YOUR_USERNAME\Public\Sports Interactive\Football Manager 26\languages
```

> **หมายเหตุ**: แทนที่ `YOUR_USERNAME` ด้วยชื่อผู้ใช้ Windows ของคุณ

#### ขั้นตอนที่ 3: Clone Repository

```cmd
git clone https://github.com/ingpawat/fm2026_thai_opensource.git
cd fm2026_thai_opensource
```

#### ขั้นตอนที่ 4: แตกไฟล์ .gz

สำหรับ Windows ใช้ 7-Zip หรือ WinRAR:

```cmd
# ถ้าใช้ 7-Zip (ต้องติดตั้งแล้ว)
"C:\Program Files\7-Zip\7z.exe" x *.gz

# หรือ ดาวน์โหลด 7-Zip จากที่นี่:
# https://www.7-zip.org/
```


---

## 📦 การส่ง Pull Request

### macOS

#### ขั้นตอนที่ 1: สร้าง Zip ของไฟล์ที่แก้ไข

```bash
# สร้างไฟล์ zip
zip -r fm2026_thai_translated.zip *.ltf *.ltc *.json

# ตรวจสอบขนาดไฟล์
ls -lh fm2026_thai_translated.zip
```

#### ขั้นตอนที่ 2: เพิ่มการเปลี่ยนแปลงไปยัง Git

```bash
# ดูสถานะ
git status

# เพิ่มไฟล์ทั้งหมดที่เปลี่ยนแปลง
git add .

# Commit
git commit -m "Thai translation: update [description of changes]"
```

#### ขั้นตอนที่ 3: Push ไปยัง Branch ของคุณ

```bash
# สร้าง branch ใหม่
git checkout -b thai-translation-update

# Push ไปยัง GitHub
git push -u origin thai-translation-update
```

#### ขั้นตอนที่ 4: สร้าง Pull Request

ไปที่ GitHub repository และคลิก "Create Pull Request"

### Windows

#### ขั้นตอนที่ 1: สร้าง Zip ของไฟล์ที่แก้ไข

```cmd
# ใช้ PowerShell ในการสร้าง Zip
Compress-Archive -Path *.ltf, *.ltc, *.json -DestinationPath fm2026_thai_translated.zip

# หรือใช้ 7-Zip
"C:\Program Files\7-Zip\7z.exe" a fm2026_thai_translated.zip *.ltf *.ltc *.json
```

#### ขั้นตอนที่ 2: เพิ่มการเปลี่ยนแปลงไปยัง Git

```cmd
# ดูสถานะ
git status

# เพิ่มไฟล์ทั้งหมดที่เปลี่ยนแปลง
git add .

# Commit
git commit -m "Thai translation: update [description of changes]"
```

#### ขั้นตอนที่ 3: Push ไปยัง Branch ของคุณ

```cmd
# สร้าง branch ใหม่
git checkout -b thai-translation-update

# Push ไปยัง GitHub
git push -u origin thai-translation-update
```

#### ขั้นตอนที่ 4: สร้าง Pull Request

ไปที่ GitHub repository และคลิก "Create Pull Request"

---

## 📝 File Structure

```
fm2026_thai_opensource/
├── README.md                      # ไฟล์นี้
├── prompt.md                      # คำสั่ง AI สำหรับการแปล
├── fm2026_thai_opensource.ltf     # ไฟล์แปล Main
├── fm2026_thai_opensource.ltc     # ไฟล์ Comments (ถ้ามี)
└── .gitignore                     # ไฟล์ที่จะเพิ่มเข้า Git
```

---

## ⚠️ สิ่งที่ต้องระวัง

- ✅ **ให้แน่ใจว่า** แก้ไขเฉพาะเนื้อหาที่แปลเท่านั้น
- ✅ **เก็บไว้** รูปแบบ `.ltf` และ `.ltc` ให้เหมือนเดิม
- ✅ **ตรวจสอบ** ไฟล์ก่อนการ commit
- ❌ **อย่าแก้ไข** `.gitignore` โดยไม่จำเป็น
- ❌ **อย่า Commit** ไฟล์ .gz ที่ไม่ได้แตก

---

## 🔗 ลิงก์ที่มีประโยชน์

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Pull Request Guide](https://docs.github.com/en/pull-requests)
- [Claude API Documentation](https://docs.anthropic.com/)
- [FM26 Thai Language Pack Repository](https://github.com/ingpawat/fm2026_thai_opensource)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 ingpawat

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
