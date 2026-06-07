# Skill: gen_scripts — Tạo Kịch Bản & Production Pack cho TikTok Affiliate Video

## MỤC ĐÍCH

Skill này tạo ra 2 file output cho mỗi batch video TikTok affiliate:
1. **`scripts.md`** — Kịch bản hoàn chỉnh cho từng video (Prehook → Transition → Body → B-roll → CTA) kèm phân tích tư duy chiến lược
2. **`production_pack.md`** — Bộ "ready-to-paste" gồm 3 phần: D (prompts ảnh tĩnh), B (script prehook chia 8s), C (script body chia 8s)

## VỊ TRÍ OUTPUT

Output được lưu tại: `task/video_{NNN}/` trong đó `{NNN}` là số tự động tăng dần (001, 002, 003...).

**Quy tắc auto-increment:**
1. Quét thư mục `task/` để tìm tất cả folder có pattern `video_*`
2. Lấy số lớn nhất hiện có → tăng thêm 1
3. Nếu chưa có folder nào → bắt đầu từ `video_001`

Ví dụ: nếu đã có `video_001`, `video_002` → tạo `video_003/scripts.md` và `video_003/production_pack.md`

---

## BƯỚC 1: KIỂM TRA & THU THẬP ĐẦU VÀO

Trước khi bắt đầu viết kịch bản, PHẢI hỏi người dùng TẤT CẢ các câu hỏi sau **trong 1 lần duy nhất**. Với mỗi câu hỏi, nếu đáp án là loại đã được định nghĩa trong tài liệu nền tảng → đề xuất luôn các options. Nếu đáp án mở → đưa ra vài gợi ý.

### Danh sách câu hỏi (hỏi 1 lần):

**Câu hỏi 1: Sản phẩm**
> Bạn muốn tạo kịch bản cho sản phẩm nào? Hãy cung cấp:
> - Tên sản phẩm
> - Hoạt chất chính
> - Công dụng chính
> - Giá bán hiện tại
> - Thương hiệu (có phải Black-owned không?)
>
> *Gợi ý: Ví dụ "Floraviva Rhodiola Rosea Capsules — hoạt chất Rhodiola Rosea — hỗ trợ giảm stress, cân bằng cortisol — $19.99 — Black-owned"*

**Câu hỏi 2: Nhóm khách hàng mục tiêu**
> Nhóm khách hàng mục tiêu của bạn là ai?
> - Quốc tịch / chủng tộc
> - Giới tính
> - Độ tuổi
> - Lifestyle (busy, stressed, health-conscious,...)
> - Vấn đề đang gặp phải
> - Mong muốn cải thiện
>
> *Gợi ý: Ví dụ "Phụ nữ Mỹ gốc Phi, 38-55 tuổi, bận rộn, stress kéo dài, mất ngủ, mệt mỏi mãn tính, muốn lấy lại năng lượng và sức khỏe"*

**Câu hỏi 3: Body Avatar cố định (Persona)**
> Bạn chọn loại persona nào cho nhân vật chính (body avatar)? Hãy chọn loại persona và đặt tên + mô tả ngoại hình:
> - **Doctor** — Bác sĩ chuyên khoa (uy tín y khoa, trang phục scrub/áo blouse, stethoscope)
> - **Wellness Expert** — Chuyên gia sức khỏe dân sự (gần gũi, thực tế, phong cách lifestyle)
> - **Traditional Holistic Healer** — Thầy thuốc cổ truyền (tri thức cổ xưa, huyền bí, di sản văn hóa)
>
> *Gợi ý: Ví dụ "Doctor — Dr. Monique Carter, nữ bác sĩ Mỹ gốc Phi 42 tuổi, áo scrub xanh navy, đeo ống nghe"*

**Câu hỏi 4: Số lượng video**
> Bạn muốn tạo bao nhiêu kịch bản video? (tối thiểu 2)
>
> *Gợi ý: 2-4 video là phổ biến nhất*

**Câu hỏi 5: Body Avatar Concept (cho mỗi video)**
> Với mỗi video, bạn chọn concept hình ảnh nào cho body avatar?
> - **Single Avatar Closeup** — Cận mặt, nhìn thẳng camera, phòng tư vấn/clinic, ánh sáng tự nhiên
> - **Single Avatar Further On Stage** — Toàn thân trên sân khấu TED-talk, micro, backdrop chuyên nghiệp
> - **Street Interview** — Phỏng vấn đường phố, 2 nhân vật (chính + interviewer cầm mic), ngoài trời
> - **Studio Interview** — Phỏng vấn studio podcast, 2 nhân vật, phòng studio tối ấm, microphone chuyên nghiệp

**Câu hỏi 6: Prehook Concept (cho mỗi video)**
> Với mỗi video, bạn muốn dùng prehook concept nào?
> - **Funeral** — Đám tang, người thân khóc nghẹn, selfie rung lắc, cảm xúc hối hận/mất mát
> - **News Anchor** — Bản tin thời sự Breaking News, MC chuyên nghiệp, banner đỏ, cảm giác bị kiểm duyệt
> - **Historical Storytelling** — Kể chuyện lịch sử, hình ảnh B&W/sepia, nhân vật cổ xưa, bi kịch + thành phần bí ẩn
> - **Không có prehook** — Body avatar nói trực tiếp từ đầu (phù hợp Street Interview hoặc Studio Interview khi muốn câu hỏi mở đầu tự nhiên)

**Câu hỏi 7: Loại Script (cho mỗi video)**
> Với mỗi video, bạn chọn loại script nào?
> - **Type 1: Silent Symptom** — Dấu hiệu âm thầm → Nguyên nhân bị che giấu → Hé lộ giải pháp tự nhiên. Build trust sâu, nhịp chậm, 6 phần.
> - **Type 2: Symptom Labeling** — Gọi tên triệu chứng liên tục → Giọng chuyên gia → Giải pháp cấp bách. Nhịp nhanh, dồn dập, 4 phần.
> - **Type 3: Myth Busting** — Phá vỡ niềm tin sai → Sự thật cổ xưa → Chứng thực + Khan hiếm. Đánh vào niềm tin, 7 phần.

### Quy tắc thu thập:
- Hỏi TẤT CẢ câu hỏi trong 1 message duy nhất
- Nếu người dùng đã cung cấp sẵn một số thông tin trong request ban đầu → không hỏi lại, chỉ hỏi phần thiếu
- Nếu người dùng chỉ nói "dùng lại từ task trước" → đọc file scripts.md hoặc Bai_4 gần nhất trong thư mục `task/` để lấy thông tin
- Sau khi có đủ thông tin → xác nhận lại tóm tắt với người dùng trước khi bắt đầu viết

---

## BƯỚC 2: TẠO FILE `scripts.md` (Output 1)

### Cấu trúc tổng thể file:

```markdown
# Kịch Bản Hoàn Chỉnh — [Tên sản phẩm] ([Số lượng] Video)

**Body Avatar Cố Định:** [Tên persona] ([Loại concept])
**Sản phẩm:** [Tên sản phẩm]

---

## VIDEO N: [Prehook Concept] + [Body Avatar Persona] [Body Concept]

### 1. Prehook ([Concept Name])
*(Visual: Mô tả chi tiết khung cảnh, nhân vật, cảm xúc, ánh sáng, góc máy, chất lượng camera)*
> "Thoại prehook tiếng Anh..."

### 2. Đoạn Chuyển (Transition)
*(Hình ảnh: Mô tả cách chuyển cảnh — hard cut, hiệu ứng,...)*
> "Thoại chuyển cảnh tiếng Anh..."

### 3. Body (Script Type N — [Tên loại])
> "Thoại body đầy đủ tiếng Anh, chia theo từng PHẦN..."

### 4. B-roll + Lời thoại đè (Overlay)
*(Hình ảnh B-roll: Mô tả cảnh cầm sản phẩm, góc máy POV, ánh sáng)*
> *(Thoại [persona] tiếp tục đọc):* "Thoại overlay tiếng Anh..."

### 5. CTA
*(Hình ảnh: Quay lại mặt [persona])*
> "Thoại CTA tiếng Anh..."

---

### PHÂN TÍCH TƯ DUY

**0. Nhóm KH mục tiêu:** [Mô tả phân khúc cụ thể, tại sao nhóm này phù hợp]
**1. Vì sao chọn Script Type này:** [Giải thích match với persona/concept/phase, so sánh với 2 type còn lại]
  - Nỗi sợ của nhóm KH: ...
  - Thế mạnh của nhóm KH: ...
**2. Giọng điệu:** [Mô tả giọng điệu cụ thể, lý do chọn]
**3. Vì sao chọn các triệu chứng/luận điểm mở đầu:** [Giải thích từng triệu chứng]
**4. Kết nối Vấn đề → Sản phẩm:** [Mô tả logic chain từng bước]
**5. CTA đánh vào:** [Khan hiếm? Niềm tin? Sợ bỏ lỡ? Kết hợp?]

---

[Lặp lại cho các VIDEO tiếp theo]

---

## TỔNG KẾT [N] KỊCH BẢN — Phân bổ chiến lược

| Video | Persona | Concept | Script Type | Vai trò trong funnel |
|---|---|---|---|---|
| 1 | ... | ... | ... | ... |
```

### Quy tắc viết scripts.md:

**A. Quy tắc viết thoại Body (theo loại script):**

**Script Type 1 — Silent Symptom (6 phần):**
1. PHẦN 1 — Mở đầu bằng nỗi sợ/dấu hiệu bị bỏ qua (2-4 câu, 2-3 dấu hiệu)
2. PHẦN 2 — Gợi ý "có gì đó không ổn" (2-3 câu)
3. PHẦN 3 — Xác định nguyên nhân chung (2-4 câu, CHỈ 1 nguyên nhân duy nhất)
4. PHẦN 4 — Khuếch đại hậu quả có kiểm soát (cảnh báo chân thành, không hù dọa)
5. PHẦN 5 — Giới thiệu giải pháp dưới dạng "phát hiện" (không quảng cáo)
6. PHẦN 6 — Sản phẩm + lọc niềm tin (gọi tên sản phẩm + CTA)

**Script Type 2 — Symptom Labeling (4 phần):**
1. PHẦN 1 — Liệt kê triệu chứng + đóng nhãn nguyên nhân ngay lập tức (5-8 câu ngắn, lặp cấu trúc, 5-7 triệu chứng)
2. PHẦN 2 — Phá bỏ niềm tin cũ + nâng mức nguy hiểm (2-3 câu)
3. PHẦN 3 — Giải pháp dạng di sản/tự nhiên (3-4 câu)
4. PHẦN 4 — Sản phẩm + CTA dạng cảnh báo (4-6 câu)

**Script Type 3 — Myth Busting (7 phần):**
1. PHẦN 1 — Phá vỡ niềm tin phổ biến (2-3 câu, nhịp mạnh, phủ định thẳng tay)
2. PHẦN 2 — Đưa ra "thứ đúng" + so sánh vượt trội (1-2 câu)
3. PHẦN 3 — Gắn giải pháp với giá trị cổ xưa/bị che giấu (2-3 câu)
4. PHẦN 4 — Liệt kê lợi ích theo dòng cảm nhận cơ thể (3-5 câu)
5. PHẦN 5 — Chứng thực bằng con người thật (3-4 câu)
6. PHẦN 6 — Giới thiệu sản phẩm + lọc thị trường (3-5 câu)
7. PHẦN 7 — Khan hiếm + CTA cảm xúc (2-3 câu)

**B. Quy tắc viết thoại Prehook:**

**Funeral Concept (Module 5):**
- Cấu trúc 4 tầng: Thu hút & Quen thuộc → Nút thắt tò mò 1 → Gỡ nút thắt 1 → Nút thắt tò mò 2 (KHÔNG GỠ)
- Visual: Selfie rung lắc, mắt đỏ khóc, iPhone front camera quality, bối cảnh đám tang
- Tone: Nghẹn ngào, lấy hơi ngắt quãng, cảm xúc thật
- Phải nhắc tên persona body ở cuối để tạo cầu nối ("video này của Bác sĩ X")
- Đa dạng hóa: quan hệ nhân vật (chị/mẹ/chồng), loại bệnh lý, cách thể hiện hối tiếc
- Luôn dùng iPhone camera quality, handheld, slight shake

**News Anchor Concept (Module 6):**
- Cấu trúc 4 tầng: Headline context → 3 curiosity layers (tại sao lên bản tin? nói gì? chuyện gì xảy ra?) → CTA khẩn cấp
- Visual: Studio tin tức chuyên nghiệp, banner Breaking News đỏ, MC mặc blazer, cinematic broadcast lighting
- Tone: Nghiêm túc, khẩn cấp, chuyên nghiệp như CNN/Fox News
- Opening phrase: "Breaking News...", "Urgent Update...", "New Report..."
- CTA phải tạo urgency: "before they try to cover this up again"
- Ultrarealistic camera quality, KHÔNG dùng iPhone quality

**Historical Storytelling Concept (Module 7):**
- Framework: Opening hook (tragedy/mystery) → Bridge character → Bridge ingredient → Product connection → CTA
- Visual: B&W hoặc sepia, grain phù hợp thời kỳ, props/trang phục lịch sử chính xác
- Cần: Bridge Character (nhân vật lịch sử có thật hoặc plausible) + Bridge Ingredient (thành phần cầu nối từ thành phần sản phẩm)
- 3 pillar: Tragedy/Origin Story + Hidden Knowledge + Product Bridge
- Tool tạo visual: Dùng keyword libraries (Library A: style theo thời kỳ, Library B: bối cảnh, Library C: hành động)
- Break script thành micro-scene 2-3s mỗi scene

**Đoạn Chuyển (Transition):**
- Luôn có giữa prehook và body
- 1-2 câu thoại
- Hard cut (cắt cảnh dứt khoát, KHÔNG crossfade)
- Nội dung liên kết prehook với body (nhắc lại context từ prehook)

**C. Quy tắc viết Visual Description:**
- Mô tả chi tiết: nhân vật (tuổi, chủng tộc, trang phục, biểu cảm), bối cảnh (địa điểm, ánh sáng, thời gian), góc máy (selfie/chest-up/toàn thân), chất lượng (iPhone/broadcast)
- Mỗi phần cần có visual description riêng

**D. Độ dài script:**
- Mỗi script body: 350-500 từ
- Mỗi prehook: 30-80 từ
- Transition: 15-30 từ

---

## BƯỚC 3: TẠO FILE `production_pack.md` (Output 2)

### Cấu trúc file (CHỈ 3 phần — D, B, C):

```markdown
# Production Pack — [Tên sản phẩm]

---

## D. Prompts tạo Hình ảnh tĩnh (Start Frames & B-roll)

### D.1 — Prehook Video N Start Frame ([Concept])
```
[Prompt tạo ảnh start frame cho prehook, mô tả chi tiết vertical 9:16, nhân vật, bối cảnh, ánh sáng, camera quality]
```

### D.2 — Body Start Frame ([Persona] — dùng chung/riêng cho video)
```
[Prompt tạo ảnh body avatar, vertical 9:16, mô tả persona, trang phục, bối cảnh, ánh sáng]
```

### D.3 — B-Roll Sản Phẩm

**Prompt tạo ảnh B-roll (Template 05):**
```
Photorealistic close-up of a [phù hợp chủng tộc KH] hand holding a bottle right up to the camera, front label facing perfectly forward. The hand grips naturally from the side with relaxed fingers, neat nails, realistic skin texture and creases. The bottle is vertical, centered, filling ~70% of frame. Even, soft studio lighting (large softbox at 45° + fill) to avoid glare and reflections. Modern simple living background. 50–85 mm lens look, f/5.6 for full label sharpness, no motion blur. Glass edges crisp, liquid visible. Reproduce the exact label text clearly and 100% legible—no warping, no truncation, no misspellings. High resolution, sharp focus, true-to-life colors.
```

**Prompt tạo video B-roll (Template 06):**
```
Lock camera. Bottle upright. Subtle idle motion and slightly turn the bottle left and right as if showing the product to the camera.
```

---

## B. Script chia 8s + Prompt Video — PREHOOK

### VIDEO N — Prehook [Concept]

**TEMPLATE PROMPT VIDEO:**
```
[Prompt template phù hợp concept — mô tả nhân vật, tone giọng, camera movement, background]
```

**Script chia segments:**
| # | Segment dialogue | Từ |
|---|---|---|
| 1 | [segment 1] | [word count] |
| 2 | [segment 2] | [word count] |
...

---

## C. Script chia 8s + Prompt Video — BODY

### VIDEO N — Body tiếp nối [Concept] ([Persona])

**TEMPLATE PROMPT VIDEO:**
```
[Prompt template phù hợp concept — mô tả avatar, tone, camera, movement, background music: none]
```

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | [segment 1] | [word count] |
| 2 | [segment 2] | [word count] |
...
```

### Quy tắc chia segments:
- Mỗi segment: **14-17 từ** (tối ưu cho 8 giây Veo)
- Đếm chính xác số từ và ghi vào cột "Từ"
- **Quy tắc punctuation cho Street Interview và Studio Interview:** CHỈ dùng dấu phẩy trong body segments — KHÔNG dùng dấu chấm — để Veo không nhầm là nhân vật phụ nói
- Segment đầu tiên của body sau transition: gộp luôn câu transition vào

### Quy tắc viết Prompt Video Template:
- Phải mô tả: tone giọng, hướng nhìn camera, chuyển động, background music (luôn là "no background music")
- Template khác nhau tùy concept:

**Closeup:**
```
The [description of avatar] in the image speaks the following dialogue in a [tone]: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. The camera stays fixed at chest-up level. Avatar maintains eye contact with the camera. Subtle natural hand gestures only. No background music. Realistic iPhone-camera quality.
```

**On Stage (Heygen):**
```
Tone: [tone description].
Camera: fixed wide shot, avatar on TED-talk stage, three-quarter angle, NEVER faces camera directly, addresses audience.
Movement: subtle natural hand gestures while speaking. No camera zoom.
Background music: none.
Voice: [voice description].
```

**Street Interview:**
```
The [description of avatar] in the image speaks the following dialogue in a casual, real, conversational tone, like chatting with a friend on the street: "{{DIALOGUE}}"
The interviewer's hand on the right keeps holding the foam microphone tilted toward [direction], steady. The shot remains stable. No zoom. The avatar's gaze stays on the interviewer (off-frame right), not at the camera. Sunny urban ambient. No background music.
```

**Studio Interview:**
```
The [description of avatar] in the image speaks the following dialogue in a [tone]: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. Warm studio podcast lighting. The avatar sits facing slightly toward the interviewer. No background music.
```

**Funeral Prehook:**
```
The [description] in the image speaks the following dialogue with a crying, grieving, and emotional tone: "{{DIALOGUE}}"
The shot remains stable. Slight handheld camera shake. No background music. Realistic iPhone-camera quality.
```

**News Anchor Prehook:**
```
The [description] in the image speaks the following dialogue in a serious, urgent, and professional broadcast tone: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. No background music. High-quality broadcast television look.
```

### Quy tắc viết Prompt Start Frame:
- Luôn bắt đầu bằng "Photorealistic vertical 9:16..."
- Mô tả chi tiết: nhân vật, tuổi, chủng tộc, trang phục, biểu cảm, bối cảnh, ánh sáng, camera quality
- Funeral: iPhone front camera quality, outdoor cloudy, mourning
- News Anchor: broadcast TV quality, newsroom, cinematic lighting
- Closeup: iPhone camera quality, clinic/consultation room
- Street: sunny urban, handheld foam microphone, từ đầu gối trở lên
- Studio: podcast studio, warm lighting, microphone chuyên nghiệp

---

## KIẾN THỨC NỀN TẢNG (BẮT BUỘC TUÂN THỦ)

### Module 2 — Ngôn từ an toàn TikTok

**BẮT BUỘC** kiểm tra toàn bộ script sau khi viết xong. Thay thế các từ/cụm sau:

| Cần tránh | Thay bằng |
|---|---|
| heal, cure, treat, reverse, repair, fix | support, help support, promote wellness, part of a healthy routine |
| instantly, immediately, guaranteed, fast results | over time, many people notice, may help, some users experience |
| hormone imbalance, nerve damage, clogged arteries, inflammation, adrenal fatigue | energy support, healthy aging, overall wellness, daily wellness routine, healthy lifestyle support |
| your body is struggling/failing, this is dangerous, your organs are failing | many people overlook this, small habits can make a difference |
| chẩn đoán y khoa cá nhân | dùng dạng "many women", "most people", "some of my clients" |

**Tư duy đúng:**
- "khẳng định" → "gợi mở"
- "điều trị" → "hỗ trợ"
- "chẩn đoán" → "chia sẻ trải nghiệm"
- Viết như chia sẻ routine cá nhân, KHÔNG phải bác sĩ đưa kết luận y khoa

### Module 3 — Body Avatar Concept (quy tắc visual)

**Closeup:** Avatar chiếm 2/3 chiều cao khung hình, centered. Cận mặt chest-up.
**On Stage:** Avatar chiếm tối đa 3/4 chiều cao. Cảnh xa, có sân khấu, backdrop.
**Street Interview:**
- Nhân vật chính: 3/5 bên trái. Nhân vật phụ: 1/5 bên phải (chỉ cần tay cầm mic)
- Cần 2 start frame: (a) mic về phía interviewer, (b) mic về phía interviewee
- Khung hình từ đầu gối trở lên
- CHỈ dùng dấu phẩy trong prompt body
**Studio Interview:**
- Avatar chiếm 3/4 đến 4/5 chiều cao
- Avatar nằm giữa chiều ngang
- Cần 2 start frame: nhân vật chính + nhân vật phụ, hướng mặt về phía nhau
- Đan xen 2-3 phân cảnh gật đầu của nhân vật phụ
- CHỈ dùng dấu phẩy trong prompt body
- Gam màu tối ấm cho studio

### Module 4 — Avatar Personas

**Doctor:** Uy tín y khoa. Scrub/áo blouse, stethoscope. Phòng khám/clinic. Giọng: calm, warm, professional.
**Wellness Expert:** Gần gũi, lifestyle. Smart casual. Sân khấu/ngoài trời. Giọng: confident, relatable, slightly AAVE.
**Traditional Holistic Healer:** Di sản văn hóa, tri thức cổ xưa. Trang phục truyền thống. Phòng thảo dược/cabin gỗ. Giọng: slow, warm, weighted.

### Module 5 — Prehook Funeral (checklist)
- [ ] Nhân vật prehook KHÁC nhân vật body (người thân, không phải chuyên gia)
- [ ] Có nhắc tên persona body ở cuối prehook
- [ ] Visual: selfie iPhone, rung lắc, mắt đỏ, ngoài trời mây
- [ ] Tone: nghẹn ngào, ngắt quãng
- [ ] Nút thắt tò mò cuối cùng KHÔNG ĐƯỢC gỡ

### Module 6 — Prehook News Anchor (checklist)
- [ ] Banner "BREAKING NEWS" hoặc tương tự
- [ ] Opening phrase: "Breaking News..." / "Urgent Update..."
- [ ] CTA tạo urgency ("before it gets taken down again")
- [ ] Visual: broadcast TV quality, NOT iPhone
- [ ] 3 curiosity layers (giữ ít nhất 1 chưa gỡ)

### Module 7 — Prehook Historical Storytelling (checklist)
- [ ] Có Bridge Character (nhân vật lịch sử)
- [ ] Có Bridge Ingredient (thành phần cầu nối với sản phẩm)
- [ ] Visual style phù hợp thời kỳ (B&W/sepia/engraving)
- [ ] 3 pillar: Tragedy + Hidden Knowledge + Product Bridge
- [ ] Script chia thành micro-scene 2-3s

### Ngôn ngữ output
- **Script body / thoại / prompt:** Tiếng Anh (thị trường US)
- **Phân tích tư duy / chỉ dẫn visual / heading:** Tiếng Việt
- **Prompt Start Frame / Prompt Video:** Tiếng Anh

---

## CHECKLIST CUỐI CÙNG (Trước khi giao output)

- [ ] Tất cả script body đã qua kiểm tra ngôn từ an toàn (Module 2)
- [ ] Mỗi video có đủ: Prehook (nếu có) → Transition → Body → B-roll → CTA
- [ ] Production pack có đúng thứ tự D → B → C
- [ ] Mỗi segment trong production pack có đếm từ chính xác (14-17 từ)
- [ ] Street/Studio Interview: body segments chỉ dùng dấu phẩy
- [ ] Start frame prompts bắt đầu bằng "Photorealistic vertical 9:16..."
- [ ] Phân tích tư duy có đủ 6 mục (0-5)
- [ ] Bảng tổng kết cuối file scripts.md
- [ ] Files được lưu đúng vị trí: task/video_{NNN}/
