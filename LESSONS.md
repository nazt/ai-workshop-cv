# Lessons Learned

บันทึกสิ่งที่เรียนรู้จากการทำงาน ใช้เป็น reference สำหรับครั้งหน้า

---

## GitHub Markdown

> เรียนรู้จาก: AI Diary 7 ธันวาคม 2568

### ปัญหา
GitHub markdown **ไม่ render line breaks** แบบ plain text

### วิธีที่ไม่ work

```markdown
❌ plain text ติดกัน
**วันที่**: 7 ธันวาคม
**เวลา**: 14:50

❌ blockquote
> บรรทัด 1
> บรรทัด 2
```

### วิธีที่ work

```markdown
✅ Bullet list (แนะนำ)
- **วันที่**: 7 ธันวาคม
- **เวลา**: 14:50

✅ Table
| Key | Value |
|-----|-------|
| วันที่ | 7 ธันวาคม |

✅ HTML <br>
**วันที่**: 7 ธันวาคม<br>
**เวลา**: 14:50
```

### Rule of Thumb
> ต้องการหลายบรรทัด → **ใช้ bullet list** เป็นตัวเลือกแรก

---

## GitHub Issue

> เรียนรู้จาก: AI Diary 7 ธันวาคม 2568

### ปัญหา
Issue ยาวเกินไป คนอ่านไม่หมด

### แนวทาง
- เขียนสั้น กระชับ
- ใช้ภาษาที่ user เข้าใจ (ถ้า user ใช้ไทย → เขียนไทย)
- มี context พอ แต่ไม่ใช่ essay
- ใช้ checklist สำหรับ track progress

### โครงสร้างที่ดี
```markdown
## สรุป
1-2 ประโยค

## เปลี่ยนแปลงหลัก
- ข้อ 1
- ข้อ 2

## Checklist
- [ ] task 1
- [ ] task 2
```

---

## Working with AI

> เรียนรู้จาก: AI Diary 7 ธันวาคม 2568

### Tips สำหรับ User
- **บอก requirement ครบตั้งแต่แรก** - จะเร็วกว่าบอกทีละนิด
- **Feedback ทันที** - บอกเลยว่าชอบ/ไม่ชอบ
- **ตรงๆ ดีกว่าอ้อม** - AI รับ feedback ตรงๆ ได้

### Tips สำหรับ AI
- **ถามให้ครบก่อนทำ** - Git? Issue? ภาษาอะไร?
- **รู้ข้อจำกัดของ platform** - เช่น GitHub markdown quirks
- **Preview ก่อน commit** - ถ้าไม่แน่ใจ

---

*Last updated: 7 ธันวาคม 2568*
