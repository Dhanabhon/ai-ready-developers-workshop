# AI-Ready Developers Workshop

เอกสารและทรัพยากรประกอบ workshop สำหรับนักพัฒนาที่ต้องการทำงานร่วมกับ AI Coding Agent (Google Antigravity, OpenCode, Cursor, Claude Code, Codex, ZCode และอื่น ๆ)

## เตรียมความพร้อมก่อนเริ่ม (Prerequisites)

ผู้เข้าร่วมอบรม**ต้องเตรียมเครื่องให้เสร็จก่อนวัน workshop** ตามเอกสารนี้ — ใช้เวลาราว 1–2 ชั่วโมง รองรับทั้ง Windows และ macOS:

**[เปิดเอกสารเตรียมความพร้อม → dhanabhon.github.io/ai-ready-developers-workshop](https://dhanabhon.github.io/ai-ready-developers-workshop/)**

หรือสแกน QR ด้านล่างเพื่อเปิดบนมือถือ:

<a href="https://shor10.co/ai-dev-workshop-prereqs">
  <img src="docs/assets/prerequisites-qr.png" alt="QR code ไปยังเอกสารเตรียมความพร้อม" width="180">
</a>

เนื้อหาครอบคลุมตามลำดับ 00–10:

- สเปกเครื่องที่แนะนำ และการเตรียมระบบปฏิบัติการ (WSL2 บน Windows / Homebrew บน macOS)
- พื้นฐานคำสั่ง Linux สำหรับผู้เริ่มต้นใช้ WSL
- การสมัครบัญชีแพลตฟอร์ม AI เน้น Free tier ก่อน (Google Antigravity, Cursor, OpenCode) ส่วนแผนเสียเงินเป็นทางเลือก (Z.ai/ZCode, Claude, ChatGPT)
- การสมัครบัญชีแพลตฟอร์มนักพัฒนา (GitHub, Vercel, Supabase)
- การติดตั้ง AI Coding CLI, rtk, Skills (Superpowers) และการ symlink skills ข้ามแพลตฟอร์ม
- การเชื่อมต่อ Vercel (CLI, plugin, MCP) และเช็กลิสต์ตรวจความพร้อมก่อนวันงาน

## คู่มือระหว่างเรียน (Build Guide)

คู่มือ build-along สร้างระบบ TDC e-Asset ตาม 11 milestones ตั้งแต่ตั้งโปรเจกต์จนขึ้น Production ใช้เปิดตามระหว่างทำ workshop:

**[เปิด Build Guide → dhanabhon.github.io/ai-ready-developers-workshop/workshop](https://dhanabhon.github.io/ai-ready-developers-workshop/workshop/)**

## Demo Project (ระบบตัวอย่างที่สร้างเสร็จแล้ว)

ระบบ TDC e-Asset ฉบับสมบูรณ์ที่สร้างด้วยแนวทางเดียวกับ workshop นี้ ใช้ดูเป็นตัวอย่างว่าปลายทางหน้าตาเป็นอย่างไร หรือเปิดโค้ดเทียบตอนติดขัดระหว่างทำ:

- **ลองใช้งานจริง:** [tdc-e-asset-rho.vercel.app](https://tdc-e-asset-rho.vercel.app)
- **ซอร์สโค้ด:** [github.com/Dhanabhon/tdc-e-asset](https://github.com/Dhanabhon/tdc-e-asset)

จุดที่ควรเปิดดูเป็นพิเศษ เพราะเป็นบทเรียนหลักของ workshop:

- `AGENTS.md` และ `CLAUDE.md` คือสัญญากลางที่ทำให้ AI agent ต่างค่ายรับงานต่อกันได้ (บริบทอยู่ในรีโป ไม่ใช่ในแชต)
- `supabase/migrations/` เก็บ SQL ทุกไฟล์ไว้ในรีโป รวมถึง Stored Procedure ที่ใช้ `FOR UPDATE` row lock กันปัญหาแย่งยืมพร้อมกัน
- `docs/architecture_spec.md` คือแผนที่วางไว้ตั้งแต่ก่อนเขียนโค้ด เทียบได้กับ `docs/PLAN.md` ที่เราสร้างใน M1

> ระบบตัวอย่างมีฟีเจอร์มากกว่าที่ทำทันในหนึ่งวัน (เช่น รายงานมูลค่าทางบัญชี การแจ้งเตือนเกินกำหนดคืน) เป้าหมายของวัน workshop คือ MVP ตาม 11 milestones ส่วนที่เหลือคือแนวทางต่อยอด

## Design Mockups (ทางเลือก)

UI mockups ของระบบ TDC e-Asset (หน้า Dashboard, เวอร์ชันมือถือ, โลโก้ และภาพปกสไลด์) สำหรับผู้เข้าอบรมที่อยากได้ design สำเร็จรูปเป็นแนวทาง จะเปิดดูในเบราว์เซอร์ หรือส่งไฟล์ภาพให้ AI agent ดูเพื่อสร้าง UI ตามก็ได้:

**[เปิด Design Mockups](https://dhanabhon.github.io/ai-ready-developers-workshop/design/asset-management-mockups.dc.html)** · ไฟล์ภาพรายชิ้นอยู่ใน [docs/design/assets/](docs/design/assets/)

> ไฟล์ต้นฉบับอยู่ที่ [docs/prerequisites.html](docs/prerequisites.html) และ [docs/workshop/](docs/workshop/) — แก้ไขแล้ว push ขึ้น `main` ได้เลย GitHub Pages (เสิร์ฟจากโฟลเดอร์ `/docs`) จะ rebuild ให้อัตโนมัติภายในราว 1 นาที
