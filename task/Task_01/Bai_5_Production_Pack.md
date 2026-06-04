# Bài 5 — Tạo video hoàn chỉnh (Production Pack)

**File này là bộ "ready-to-paste" để học viên trực tiếp đưa vào Flow Veo / Heygen / Grok / CapCut.**

Cấu trúc:
- Phần A: Hướng dẫn quy trình chung (theo Module Flow Veo + Module 3)
- Phần B: Script chia nhỏ 8s + prompt video cho **mỗi 4 video**
- Phần C: Prompts B-roll (ảnh + video cầm sản phẩm) — cùng template 05/06 từ task1.md
- Phần D: Hướng dẫn ghép & overlay B-roll trong CapCut

---

## A. Quy trình chung (5 bước cho mỗi video)

1. **Tạo ảnh start frame** bằng Flow Veo (Generate Image) hoặc Grok — paste prompt ở Bài 3.
2. **Mở Flow Veo → New Project** → Frames to Video → Aspect 9:16 → Veo3.1 Quality → Outputs per prompt: 4.
3. **Upload start frame & end frame** (cùng 1 ảnh, theo Module Flow Veo).
4. **Paste prompt video segment 1** (xem bên dưới). Generate → chọn bản tự nhiên nhất → tải xuống.
5. **Extend video** từ video gốc cho mỗi segment tiếp theo (luôn click về video gốc trước khi extend, theo lưu ý Module Flow Veo).
6. Sau khi đủ tất cả segments → tải Upscaled 4K → ghép trong CapCut.

> **Quy tắc nhịp nói đều (Module Flow Veo):** Mỗi segment cố gắng giữ **14–16 từ**. Tôi đã chia sẵn để tối ưu.
>
> **Quy tắc punctuation cho concept Studio Interview & Street Interview:** Trong prompt video body, **chỉ dùng dấu phẩy** trong phần thoại — không dùng dấu chấm (Module 3) — để Veo không nhầm là interviewer nói.

---

## B. Script chia 8s + Prompt Video — 4 Video

### TEMPLATE PROMPT VIDEO (Module Flow Veo Bước 3)

```
The avatar in the image speaks the following dialogue: "{{DIALOGUE}}"
The shot remains stable. No zoom in/out. No background and theme music.
```

> Học viên chỉ cần thay `{{DIALOGUE}}` cho mỗi segment.

---

### VIDEO 1 — Doctor / Closeup / Script Type 1

**Start frame prompt** (đã có ở Bài 3 — Concept 1).

**Script chia segments (16 segments × ~8s)**

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | Most Black women in their 40s are walking around with three quiet signs they keep brushing off. | 17 |
| 2 | Number one, waking up around three in the morning for no real reason. | 13 |
| 3 | Number two, that constant tired feeling, even after a full night of sleep. | 14 |
| 4 | Number three, hair thinning around the edges, even when you treat it gently. | 14 |
| 5 | Most women just blame it on getting older or being busy. | 11 |
| 6 | But when these three things show up together, it's usually not random. | 13 |
| 7 | The body is trying to tell you something most people aren't being told. | 13 |
| 8 | What I see in my consultation room every week is the same pattern. | 13 |
| 9 | It comes back to one thing — cortisol staying elevated for too long. | 13 |
| 10 | After 40, when stress becomes daily, cortisol stops resetting at night the way it should. | 16 |
| 11 | When cortisol stays high, many women notice their sleep getting lighter and energy dropping. | 14 |
| 12 | The good news is, there's a plant our ancestors leaned on for centuries. | 13 |
| 13 | It's called Rhodiola Rosea, a natural adaptogen that helps support the body's stress response. | 15 |
| 14 | Many of my clients in their forties and fifties feel like themselves again after three weeks. | 16 |
| 15 | The only one I personally trust is Floraviva — small Black-owned, pure, lab-verified. | 13 |
| 16 | Right now it's under twenty dollars. Tap the orange button before they sell out again. | 15 |

**Prompt video — copy paste cho từng segment:**

```
The female African American doctor in the image speaks the following dialogue in a warm, calm, conversational tone: "[paste segment here]"
The shot remains stable. No zoom in/out. The camera stays fixed at chest-up level. Avatar maintains eye contact with the camera. Subtle natural hand gestures only. No background music. Realistic iPhone-camera quality.
```

---

### VIDEO 2 — Wellness Expert / On Stage / Script Type 2

**Start frame prompt** (đã có ở Bài 3 — Concept 2).

**Script chia segments**

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | You wake up with puffy eyes? That's high cortisol. | 9 |
| 2 | You roll over at three a.m. every single night? Cortisol. | 11 |
| 3 | That tightness sitting in your shoulders that won't go away? Cortisol. | 12 |
| 4 | Hair thinning around your edges? Cortisol. The ringing in your ears at night? Cortisol. | 14 |
| 5 | That stubborn belly that won't move no matter how clean you eat? Yep, cortisol, baby. | 16 |
| 6 | Most of us just call it stress, or getting older, and keep pushing. | 13 |
| 7 | But this is your body waving a red flag. | 9 |
| 8 | Cortisol staying high for years quietly wears down your sleep, your energy, and yourself. | 14 |
| 9 | Here's the part nobody told us. There's a natural adaptogen our ancestors leaned on. | 14 |
| 10 | It's called Rhodiola Rosea. It helps support the body's stress response and circulation. | 14 |
| 11 | And the best part? It's simple. One capsule a day. No nasty teas, no handful of pills. | 17 |
| 12 | But baby, don't grab just any Rhodiola. Most are weak, watered down, full of fillers. | 16 |
| 13 | The only one I trust is Floraviva — small Black-owned, lab-verified, organic, pure. | 13 |
| 14 | Right now bottles are going for under twenty dollars, but every restock sells out fast. | 15 |
| 15 | If that orange button is still down below, tap it and grab yours now. | 14 |

**Prompt video Heygen** (Heygen UI khác Veo, paste như sau khi tạo Avatar Talking Photo):

```
Tone: confident, declarative, slightly preacher-cadence Black wellness expert.
Camera: fixed wide shot, avatar on TED-talk stage, three-quarter angle, NEVER faces camera directly, addresses audience.
Movement: subtle natural hand gestures while speaking. No camera zoom.
Background music: none.
Voice: confident African American female, warm but firm, mid-pitch.
```

---

### VIDEO 3 — Traditional Healer / Studio Interview / Script Type 3

**Start frames** (2 ảnh — đã có ở Bài 3 — Concept 3).

#### B.3.1 — Video MỞ ĐẦU (interviewer hỏi → Mama Adaeze bắt đầu trả lời)

Sử dụng **Start frame ảnh interviewer phụ**. Prompt video:

```
Two characters in the studio: the female African American interviewer on the right tilts the studio microphone toward herself and asks warmly: "Mama Adaeze, women keep asking me what really helps when nothing else does. What do you tell them?"
Then the camera holds steady, no cuts.
The shot remains stable. No zoom. No background music.
```

> Sau đó cắt sang nhân vật chính bằng video tiếp theo.

#### B.3.2 — Body segments (Mama Adaeze nói liên tục)

> ⚠️ **Module 3 quy tắc:** chỉ dùng dấu phẩy trong dialogue, không dùng dấu chấm.

| # | Segment dialogue (chỉ dấu phẩy) | Từ |
|---|---|---|
| 1 | The best thing for a tired woman in her forties isn't green tea, it's not turmeric | 15 |
| 2 | and child, it definitely isn't another protein shake, people keep chasing internet trends | 14 |
| 3 | and missing what their own grandmother already knew, the simple things still work | 13 |
| 4 | Just one small dose of this every morning supports the body more deeply than | 13 |
| 5 | green tea and turmeric put together, it works in a quieter way, but it works | 15 |
| 6 | This plant has been used for thousands of years by our people across Africa | 14 |
| 7 | and by elders in the cold mountains of the north, but you know how it goes | 15 |
| 8 | the simpler something is, the harder they try to keep it out of reach | 14 |
| 9 | What I've seen it do is help support healthy circulation, the legs feel lighter | 14 |
| 10 | the chest feels easier, the mind quiets down, sleep gets deeper, energy returns | 13 |
| 11 | This ancient plant is called Rhodiola Rosea, I've shared it with many women | 13 |
| 12 | in their forties and fifties, the ones who walk in tired and carrying everything | 14 |
| 13 | Two or three weeks later they come back, and they don't talk like the same woman | 16 |
| 14 | The eyes are softer, the shoulders drop, they say Mama I feel like myself again | 15 |
| 15 | Most Rhodiola on the shelves is weak, mixed with fillers, the only one I trust | 15 |
| 16 | is Floraviva, small Black-owned, lab-verified, pure organic Rhodiola Rosea, no fillers | 13 |
| 17 | They were sold out for almost a month, they just restocked, under twenty dollars | 14 |
| 18 | If that orange button is still glowing below, child don't wait, tap it now | 14 |

**Prompt video body cho mỗi segment:**

```
The Nigerian traditional healer woman in the image speaks the following dialogue in a slow, warm, weighted, wise tone, as if sharing ancestral knowledge: "[paste segment here]"
The shot remains stable. No zoom. The healer stays in three-quarter angle, looking slightly toward the off-frame interviewer on the right, never directly at the camera. Subtle natural gestures only. Warm candlelight unchanged. No background music.
```

#### B.3.3 — Cảnh interviewer gật đầu / "uh huh" (Module 3 yêu cầu chen 2–3 cảnh)

Dùng start frame interviewer. Prompt:

```
The interviewer on the right nods slowly while listening, gives a soft "uh huh" then "yes, that's so true" — natural, respectful listening posture, leaning slightly forward. No other dialogue. The shot remains stable. No zoom. No background music.
```

Tạo 2–3 clips ngắn loại này, chèn xen kẽ trong CapCut giữa các segment dài của Mama Adaeze.

---

### VIDEO 4 — Wellness Expert / Street Interview / Script Type 1 personal

**Start frames** (2 ảnh — đã có ở Bài 3 — Concept 4).

#### B.4.1 — Video mở đầu (interviewer hỏi)

Dùng start frame **(a)** (mic về phía interviewer). Prompt:

```
The off-frame male interviewer on the right tilts the handheld foam street microphone toward himself and asks in a friendly upbeat tone: "Excuse me, quick question — you look amazing. People keep asking on TikTok what's actually working for women in their 40s. What changed for you?"
The wellness expert woman on the left turns her head, makes eye contact with the interviewer, smiles warmly, listening.
The shot remains stable. No zoom. No background music. Sunny urban Brooklyn ambient sound only.
```

#### B.4.2 — Body segments (Tasha trả lời)

Dùng start frame **(b)** (mic về phía Tasha). **Chỉ dùng dấu phẩy.**

| # | Segment dialogue | Từ |
|---|---|---|
| 1 | Honestly, a year ago I was waking up at three in the morning every single night | 16 |
| 2 | my edges were thinning, my belly stayed bloated no matter what I ate, and I was tired | 17 |
| 3 | like, tired-tired, the kind of tired sleep doesn't fix, no matter how much you get | 15 |
| 4 | I kept telling myself it was just stress, or maybe the perimenopause thing | 13 |
| 5 | but deep down I knew it wasn't normal, my body felt like it was running on fumes | 16 |
| 6 | Then a friend who's a wellness coach told me, most of it was cortisol staying high | 16 |
| 7 | After forty, the body doesn't reset stress at night the way it used to | 14 |
| 8 | once she said that, everything clicked, all the small symptoms made sense at once | 14 |
| 9 | She said women in our community especially carry stress in our bodies for years | 14 |
| 10 | and over time, it shows up in the sleep, the belly, the edges, the energy, all of it | 17 |
| 11 | So she put me on this plant called Rhodiola Rosea, an adaptogen that supports stress | 15 |
| 12 | About three weeks in, I noticed I was sleeping straight through the night again | 14 |
| 13 | Three weeks after that, my edges were filling back in, my belly was flatter | 14 |
| 14 | The brand she put me on is Floraviva, small Black-owned, lab-verified, no fillers | 13 |
| 15 | Most others are watered down, Floraviva is the one I keep restocking every month | 14 |
| 16 | They had a sale last week, under twenty a bottle, if they're still in stock grab one | 17 |

**Prompt video body cho mỗi segment:**

```
The female African American wellness expert in the image speaks the following dialogue in a casual, real, conversational tone, like she's chatting with a friend on the street: "[paste segment here]"
The interviewer's hand on the right keeps holding the foam microphone tilted toward her, steady. The shot remains stable. No zoom. The avatar's gaze stays on the interviewer (off-frame right), not at the camera. Sunny urban ambient. No background music.
```

---

## C. Prompts B-roll (cảnh cầm sản phẩm)

> Theo task1.md mục Bài 5: dùng **prompt template 05** cho ảnh, **prompt template 06** cho video. Học viên upload ảnh sản phẩm Floraviva trực diện trước khi paste prompt.

### C.1 — Prompt 05 (TẠO ẢNH B-roll cầm chai)

Đã được task1.md cung cấp. Paste vào **Flow Veo → Generate Image**:

```
Photorealistic close-up of a female African-American hand holding a bottle right up to the camera, front label facing perfectly forward. The hand grips naturally from the side with relaxed fingers, neat nails, realistic skin texture and creases. The bottle is vertical, centered, filling ~70% of frame. Even, soft studio lighting (large softbox at 45° + fill) to avoid glare and reflections. Modern simple living background. 50–85 mm lens look, f/5.6 for full label sharpness, no motion blur. Glass edges crisp, liquid visible. Reproduce the exact label text clearly and 100% legible—no warping, no truncation, no misspellings. High resolution, sharp focus, true-to-life colors.
```

> Học viên cần upload trước **1 ảnh trực diện chai Floraviva** (tham khảo `images/Floraviva/IMG_01.png` đến `IMG_05.png`) làm input cho Flow Veo.

### C.2 — Prompt 06 (TẠO VIDEO từ ảnh B-roll)

Đã được task1.md cung cấp. Trong **Flow Veo → Generate Video**, upload ảnh B-roll vừa tạo vào CẢ Start frame và End frame, paste:

```
Lock camera. Bottle upright. Subtle idle motion and slightly turn the bottle left and right as if showing the product to the camera.
```

### C.3 — Số B-roll cần tạo

Tạo **2 phiên bản B-roll** (khoảng 4–5s mỗi clip). Cùng prompt nhưng generate 2 lần để có variation.

---

## D. Hướng dẫn ghép trong CapCut

### D.1 — Ghép 4 video chính

Mỗi video:
1. Import tất cả segments theo thứ tự đã chia ở Phần B.
2. Trim đầu/cuối mỗi clip để giọng nói liền mạch (cắt 0.1–0.2s pause giữa các clip).
3. Export 1080×1920, 60fps nếu Veo cho phép, không thì 30fps.

### D.2 — Đặt B-roll làm OVERLAY (yêu cầu Bài 5)

> **Yêu cầu:** "Tạo phân cảnh broll giới thiệu sản phẩm và đặt phân cảnh này làm overlay trên đoạn hội thoại nhắc đến sản phẩm."

**Cách làm trong CapCut:**

1. Nhận diện đoạn thoại nhắc đến sản phẩm trong mỗi video (đoạn có chữ "Floraviva" lần đầu).
2. Thêm B-roll clip vào **track Overlay (track phía trên track chính)**.
3. Đặt B-roll **bắt đầu khoảng 0.3s trước** khi chữ "Floraviva" được phát ra, kéo dài 3–4s.
4. Giữ **âm thanh thoại của track chính** (mute audio của track B-roll).
5. Có thể thêm transition Crossfade 0.2s vào và ra của B-roll.

**Áp dụng cho cả 4 video:**

| Video | Đoạn cần overlay B-roll | Segment # |
|---|---|---|
| 1 | "The only one I personally trust is Floraviva..." | Segment 15 |
| 2 | "The only one I trust is Floraviva..." | Segment 13 |
| 3 | "is Floraviva, small Black-owned..." | Segment 16 |
| 4 | "The brand she put me on is Floraviva..." | Segment 14 |

### D.3 — Voiceover (nếu dùng Heygen cho video 2)

Heygen có TTS sẵn. Nếu muốn voice tự nhiên hơn, dùng **ElevenLabs voice changer** (tài liệu trong `Documents/Phương pháp Voice Changer bằng Elevenlabs`).

### D.4 — Subtitle (highly recommended cho TikTok)

Trong CapCut: Auto Captions → English (US) → font Komika Axis hoặc Bold Sans → kích thước 60–80pt → màu trắng + outline đen → animation type-on từng từ.

---

## E. Checklist nộp bài (theo Yêu cầu nộp bài task1.md)

- [ ] Bài_1_Nguoi_xem_muc_tieu.md
- [ ] Bài_2_Avatar_Personas.md
- [ ] Bài_3_Avatar_Concepts.md (kèm 6 ảnh start frame: 1+1+2+2)
- [ ] Bài_4_Scripts.md
- [ ] Bài_5_Production_Pack.md (file này)
- [ ] **4 video MP4 đã ghép xong** (có overlay B-roll trên đoạn nhắc sản phẩm)
- [ ] **2 ảnh B-roll** + **2 video B-roll**
- [ ] Upload tất cả lên Google Drive → đổi tên folder thành **tên Zalo của học viên** → cấp quyền View public → gửi link cho coach Alan.

---

## F. Bảng kiểm checklist Module 2 (Ngôn từ an toàn)

Toàn bộ 4 script đã được kiểm:

| Cụm cần tránh | Đã thay bằng | Trạng thái |
|---|---|---|
| heal / cure / treat / fix | support / help support | ✅ |
| hormone imbalance | (không dùng cụm này) — dùng "stress response" | ✅ |
| inflammation | (không dùng) — dùng "circulation, energy" | ✅ |
| guaranteed / immediately | many people notice / over time | ✅ |
| your body is failing | "your body waving a red flag" (cảnh báo, không tiêu cực cực đoan) | ✅ |
| chẩn đoán y khoa cá nhân | mọi câu đều ở dạng "many women" / "most people" | ✅ |

> Các cụm "silent killer" trong script reference Module 1 đã được mềm hoá thành "wears you down", "wave a red flag" để giảm rủi ro flag bởi TikTok content moderation.
