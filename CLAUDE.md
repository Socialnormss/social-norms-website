# CLAUDE.md — social-norms-website

Static website สำหรับ Social Norms — pure HTML/CSS/JS ไม่มี build step

---

## Deploy

Push → GitHub → Vercel (auto-deploy)

```bash
# Preview local
open index.html
# หรือ
python3 -m http.server 8080

# Deploy
git add -A && git commit -m "update: ..." && git push
```

---

## Files

```
index.html          ← Landing page (all sections)
design-system.css   ← Design tokens — source of truth (อ่านก่อนแก้ style)
basic-sns-pdf.html  ← Free lead magnet (19 หน้า)
VISUAL-DIRECTION.md ← Design rationale (อ่านก่อนแก้ visual)
```

**Phase 2 pages (ยังไม่สร้าง):**
```
mentorship.html
advanced.html
about.html
free.html
```

---

## Rules

- ห้าม hard-code สี, ขนาด, spacing — ใช้ `var(--token)` จาก design-system.css เสมอ
- Amber `#D47A2A` = signal color เท่านั้น — ไม่ใช้ตกแต่ง
- สร้าง page ใหม่: copy pattern จาก index.html, link design-system.css ก่อน, ใส่ page-specific style ใน `<style>` block ใน HTML

---

## Design System

**Background layers** (deepest → shallowest):
`--bg-void` → `--bg-base` → `--bg-surface` → `--bg-raised` → `--bg-overlay`

**Section IDs in index.html:**
`#hero` → `#signal` → `#problems` → `#about` → `#mentorship` → `#advanced` → `#proof` → `#why` → `#faq` → `#cta` → `footer`

**Scroll reveal:** class `reveal` + JS IntersectionObserver → `.is-visible` on scroll
