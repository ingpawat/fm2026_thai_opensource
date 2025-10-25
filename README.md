# FM2026 Thai Language Pack

สำหรับการแปล Football Manager 2026 เป็นภาษาไทย โดยใช้ AI ในการช่วยแปล

---

## 📋 ข้อกำหนดเบื้องต้น

- Git
- Python 3.8+ (สำหรับการประมวลผล prompt.md)
- API Key จาก Claude (สำหรับการใช้ AI)
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

#### ขั้นตอนที่ 4: ตั้งค่า Environment Variable

```bash
# เพิ่ม API Key ของ Claude
export ANTHROPIC_API_KEY="your_api_key_here"
```

#### ขั้นตอนที่ 5: เริ่มแปล

```bash
# ดูรายละเอียด prompt จาก prompt.md
cat prompt.md

# เรียกใช้ AI ในการแปล fm2026_thai_opensource.ltf
python3 translate.py fm2026_thai_opensource.ltf
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

#### ขั้นตอนที่ 5: ตั้งค่า Environment Variable

```cmd
# ใน PowerShell
$env:ANTHROPIC_API_KEY="your_api_key_here"

# ใน Command Prompt
set ANTHROPIC_API_KEY=your_api_key_here
```

#### ขั้นตอนที่ 6: เริ่มแปล

```cmd
# ดูรายละเอียด prompt
type prompt.md

# เรียกใช้ AI ในการแปล
python translate.py fm2026_thai_opensource.ltf
```

---

## ✏️ ขั้นตอนการแปล

### macOS

1. **เปิดไฟล์เพื่อแตกสำรวจ**
   ```bash
   cat fm2026_thai_opensource.ltf | head -50
   ```

2. **เริ่มแปลใช้ AI**
   ```bash
   python3 translate.py fm2026_thai_opensource.ltf --ai-translate
   ```

3. **ตรวจสอบและแก้ไขไฟล์**
   - เปิดไฟล์ในเอดิเตอร์โปรดของคุณ
   - ตรวจสอบการแปล
   - แก้ไขคำที่ไม่ถูกต้อง

### Windows

1. **เปิดไฟล์เพื่อแตกสำรวจ**
   ```cmd
   type fm2026_thai_opensource.ltf | more
   ```

2. **เริ่มแปลใช้ AI**
   ```cmd
   python translate.py fm2026_thai_opensource.ltf --ai-translate
   ```

3. **ตรวจสอบและแก้ไขไฟล์**
   - เปิดไฟล์ในเอดิเตอร์ (Notepad++ หรือ Visual Studio Code แนะนำ)
   - ตรวจสอบการแปล
   - แก้ไขคำที่ไม่ถูกต้อง

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

## 🤖 การใช้ AI ในการแปล

### ข้อมูลเพิ่มเติมเกี่ยวกับ prompt.md

```bash
# ดูรายละเอียด prompt
cat prompt.md

# Copy prompt เพื่อใช้กับ Claude
cat prompt.md | pbcopy  # macOS
cat prompt.md | clip    # Windows (PowerShell)
```

### ตัวอย่าง Prompt

prompt.md ควรมีลักษณะดังนี้:

```
Translate the following Football Manager 2026 Thai localization file to Thai.
Keep all formatting, variable names, and structure intact.
Only translate the text content.

[File content here]
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

## 📞 ติดต่อและความช่วยเหลือ

ถ้ามีปัญหา:

1. ตรวจสอบ [Issues](https://github.com/ingpawat/fm2026_thai_opensource/issues)
2. สร้าง Issue ใหม่พร้อมรายละเอียด
3. ติดต่อผู้ดูแล Repository

---

**สุดท้าย: ขอบคุณสำหรับการมีส่วนร่วมในการแปล FM2026 เป็นภาษาไทย! 🇹🇭**
