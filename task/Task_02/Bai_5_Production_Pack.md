# Bài 5 — Production Pack (Quy trình tạo video & Prompts)

**File này là bộ "ready-to-paste" để học viên trực tiếp đưa vào Flow Veo / Grok / Midjourney theo đúng lý thuyết chia nhỏ video 8s (Flow Veo).**

Cấu trúc:
- Phần A: Hướng dẫn quy trình chung tạo Video bằng Veo
- Phần B: Script chia nhỏ ~8s + Prompt Video cho **PREHOOK** của 2 Video
- Phần C: Script chia nhỏ ~8s + Prompt Video cho **BODY** của 2 Video
- Phần D: Prompts tạo hình ảnh tĩnh (Start Frames & B-roll)
- Phần E: Hướng dẫn ghép trong CapCut

---

## A. Quy trình chung tạo Video (Prehook & Body) bằng Flow Veo

Theo tài liệu "Tạo body video bằng Flow Veo", quy trình này áp dụng cho **bất kỳ đoạn hội thoại nào dài hơn 8 giây** (bao gồm cả Prehook và Body):

1. **Tạo ảnh start frame** bằng Flow Veo (Generate Image) hoặc Grok — sử dụng prompt ở Phần D.
2. **Mở Flow Veo → New Project** → Frames to Video → Aspect 9:16 → Veo3.1 Quality → Outputs per prompt: 4.
3. **Upload start frame & end frame** (cùng 1 ảnh) để giữ mặt nhân vật ổn định.
4. **Paste prompt video segment 1** (xem Phần B và C). Generate → chọn bản tự nhiên nhất → tải xuống (Video gốc).
5. **Extend video** từ video gốc cho mỗi segment tiếp theo (Lưu ý: Luôn cuộn lên và click chọn về **video gốc/hook** trước khi bấm Extend cho câu tiếp theo để tránh giảm chất lượng).

---

## B. Script chia 8s + Prompt Video — PREHOOK (2 Video)

Giống như Body, thoại của Prehook cũng cần được chia nhỏ để đảm bảo AI Veo xử lý khẩu hình tự nhiên trong giới hạn 8s.

### VIDEO 1 — Prehook Funeral (Người phụ nữ khóc trong đám tang)

**TEMPLATE PROMPT VIDEO (Flow Veo):**
```
The African American woman in the image speaks the following dialogue with a crying, grieving, and emotional tone: "{{DIALOGUE}}"
The shot remains stable. Slight handheld camera shake. No background music. Realistic iPhone-camera quality.
```

**Script chia segments:**
| # | Segment dialogue | Từ |
|---|---|---|
| 1 | My sister, she could still be here with us today. | 10 |
| 2 | If only I didn't think her waking up at three a.m. | 11 |
| 3 | and being completely exhausted was just her being too busy with the family. | 13 |
| 4 | I wish to God I had shown her this video from Dr. Carter sooner. | 14 |

---

### VIDEO 2 — Prehook News Anchor (Bản tin thời sự)

**TEMPLATE PROMPT VIDEO (Flow Veo):**
```
The female African American news anchor in the image speaks the following dialogue in a serious, urgent, and professional broadcast tone: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. No background music. High-quality broadcast television look.
```

**Script chia segments:**
| # | Segment dialogue | Từ |
|---|---|---|
| 1 | Breaking News. A health warning for women over forty was recently pulled from multiple platforms | 15 |
| 2 | after exposing the hidden cause behind chronic exhaustion. We've managed to recover | 12 |
| 3 | the deleted segment from Dr. Carter. Watch this right now, before it gets taken down again. | 16 |

---

## C. Script chia 8s + Prompt Video — BODY (2 Video)

**TEMPLATE PROMPT VIDEO (Flow Veo):**
```
The female African American doctor in the image speaks the following dialogue in a warm, calm, conversational tone: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. The camera stays fixed at chest-up level. Avatar maintains eye contact with the camera. Subtle natural hand gestures only. No background music. Realistic iPhone-camera quality.
```

### VIDEO 1 — Body tiếp nối Concept Funeral (Dr. Monique Carter)

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | What that family is going through is a heartbreak, but the painful truth is | 14 |
| 2 | I see the exact same warning signs almost every day in my clinic. | 13 |
| 3 | Most Black women in their forties are walking around with three quiet signs | 13 |
| 4 | they keep brushing off. Number one, waking up around three in the morning for no real reason. | 17 |
| 5 | Number two, that constant tired feeling, even after a full night of sleep. | 13 |
| 6 | And number three, an overall feeling of being off that they just blame on getting older. | 16 |
| 7 | What I see is always the same pattern, cortisol staying elevated for too long. | 14 |
| 8 | When stress becomes your daily background, your body stops resetting at night. | 12 |
| 9 | Over time, it quietly wears a woman down. The good news is, | 12 |
| 10 | there's a plant our ancestors leaned on for centuries called Rhodiola Rosea. | 12 |
| 11 | It's a natural adaptogen that helps support the body's response to stress. | 12 |
| 12 | Many of my clients come back saying they finally feel like themselves again. | 13 |
| 13 | Calmer mornings, deeper sleep, and more even energy. But listen to this carefully. | 13 |
| 14 | A lot of Rhodiola on the market is watered down. The only one I personally trust | 16 |
| 15 | is Floraviva, a small Black-owned company that keeps it pure and organic. | 12 |
| 16 | They just restocked. Right now it's under twenty dollars for a full month. | 13 |
| 17 | If you see the orange button below, tap it before they sell out again. | 14 |
| 18 | Take care of yourself, so you can be there for them. | 11 |

---

### VIDEO 2 — Body tiếp nối Concept News Anchor (Dr. Monique Carter)

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | I'm not surprised they tried to take this down, because it challenges an industry | 14 |
| 2 | that makes billions keeping us tired. If you're a woman over forty, | 12 |
| 3 | pay close attention to these three signs. Waking up at three a.m. consistently. | 13 |
| 4 | Feeling drained even after eight hours of sleep. And holding onto stubborn belly fat | 14 |
| 5 | that won't move. They tell you it's just getting older, but it's not. | 13 |
| 6 | It is your cortisol staying elevated for far too long. Your stress response | 13 |
| 7 | is stuck on high alert, refusing to reset at night. You don't need another generic multivitamin. | 16 |
| 8 | You need an adaptogen. Rhodiola Rosea is a plant that has been supporting | 13 |
| 9 | the human body's stress response for centuries. Women who start using it properly | 13 |
| 10 | notice their sleep deepening and that morning brain fog finally lifting. | 11 |
| 11 | The problem is finding pure Rhodiola. I strictly recommend Floraviva. | 10 |
| 12 | It's lab-verified, organic, and Black-owned, absolutely no cheap fillers. | 9 |
| 13 | They've been selling out constantly since the news broke. If the link below | 13 |
| 14 | is still showing in stock, grab a bottle for under twenty dollars. Protect your energy. | 15 |

---

## D. Prompts tạo Hình ảnh tĩnh (Start Frames & B-roll)

Bước đầu tiên luôn là phải có ảnh tĩnh (Start Frame) cho cả Prehook và Body. Copy các lệnh dưới đây vào Veo/Grok để tạo ảnh.

### 1. Prehook Video 1 Start Frame (Funeral - Khóc trong đám tang)
```
Photorealistic vertical 9:16 selfie of a 45-year-old African American woman wearing a black mourning dress, standing outdoors on a cloudy, melancholic day. She is crying, eyes red and teary, looking directly into the camera with an expression of deep regret, grief, and desperation. iPhone front camera quality, organic lighting, no beauty filters, raw and authentic. In the softly blurred background, a few silhouettes of people in black suits can be faintly seen at a funeral gathering.
```

### 2. Prehook Video 2 Start Frame (News Anchor - Bản tin thời sự)
```
Professional vertical 9:16 portrait of an authoritative African American female news anchor seated at a modern live TV newsroom desk. She wears a sharp red blazer and white blouse, looking directly into the camera with a serious, urgent expression. Nighttime city skyline backdrop, cinematic studio lighting, ultra-realistic broadcast set. A bright red lower-third news banner is visible at the bottom. The lighting mimics a high-budget national TV news broadcast like CNN or Fox News.
```

### 3. Body Start Frame (Dr. Monique Carter - Dùng chung cho cả 2 video)
```
Photorealistic vertical 9:16 portrait of a 42-year-old African American female doctor sitting at a very slight angle, almost front-facing the camera. She has a warm, empathetic, and serious expression, neatly tied professional hair, minimal makeup. She wears a clean navy blue medical scrub top with a stethoscope resting naturally around her neck. Her right hand is lifted slightly mid-gesture as if explaining a vital health point. Background: a softly out-of-focus modern, professional medical clinic room that conveys trust and expertise, featuring subtle medical equipment. Soft natural daylight from the left, realistic skin texture with natural shine, organic facial expression. Avatar fills 2/3 of frame height, centered horizontally. iPhone camera quality.
```

### 4. B-Roll Lọ Sản Phẩm (Dùng cho CapCut Overlay)
**B-Roll Video 1 (Cầm lọ sáng sớm):**
```
Photorealistic vertical 9:16 first-person POV shot holding a dark amber supplement bottle. A female African American hand is holding the bottle up against natural daylight from a nearby window. The bottle label reads "Floraviva Rhodiola Rosea - Organic & Lab Verified". The hand gently turns the bottle to show the label clearly. Cozy home interior background slightly blurred out.
```

**B-Roll Video 2 (Viên nhộng trên tay):**
```
Photorealistic vertical 9:16 first-person POV close-up. An African American woman's open palm holding a single natural, earth-toned capsule of Rhodiola supplement. The background is a slightly blurred kitchen counter with a dark amber bottle of "Floraviva" resting nearby. Sharp focus on the capsule and the texture of the hand. Natural bright daytime lighting.
```

---

## E. Hướng dẫn ghép trong CapCut

1. **Ghép Prehook:** Đưa các clip 8s của Prehook (Sau khi tải từ Veo) vào timeline.
2. **Ghép Body:** Tiếp tục đưa các clip 8s của phần Body nối ngay sau Prehook. 
3. **Hard Cut:** Đảm bảo điểm nối giữa đoạn Prehook cuối cùng và Body đầu tiên là cắt cảnh dứt khoát (Hard cut). Không dùng hiệu ứng chuyển cảnh mờ (crossfade) để giữ nhịp điệu chân thực.
4. **Cắt bỏ dead air:** Loại bỏ những khoảng lặng không cần thiết ở đầu và cuối mỗi clip 8s để giọng nói liền mạch nhất có thể.
5. **Thêm B-roll:** Kéo hình ảnh/video B-roll thả lên lớp phía trên (Overlay) của timeline vào đúng lúc Bác sĩ bắt đầu nói về lọ thuốc ("A lot of Rhodiola on the market... / The problem is finding pure Rhodiola..."). Lời thoại của bác sĩ vẫn sẽ phát bình thường ở bên dưới lớp hình ảnh B-roll này.
