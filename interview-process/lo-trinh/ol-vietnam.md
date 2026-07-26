# Lộ trình OL Vietnam — SE ~1.5 YOE

**Công ty:** OL Vietnam (Orange Logic) — Digital Asset Management (DAM)  
**Stack thường gặp:** C# / .NET (ưu tiên, không bắt buộc), SQL, Elasticsearch, AWS; media libraries quy mô lớn  
**Quy trình điển hình:** Online coding challenge (2 bài / 60') → HR (English) → Technical (fundamentals, OOP, SQL, architecture) → có thể thêm leadership / culture

> Mục tiêu: **problem-solving rõ ràng + English tốt + tư duy product DAM** (metadata, search, storage, workflow). Architecture > “chỉ biết framework”.

Xem nền tảng chung: [nen-tang-chung.md](./nen-tang-chung.md)

---

## 1. Map vòng phỏng vấn → cần học gì

| Vòng | Họ đánh giá | Prep chính |
|------|-------------|------------|
| Coding challenge | 2 problems / 60', language tự chọn | Timed NeetCode — **ưu tiên #1** |
| HR / culture | English, motivation, humility, ownership | STAR stories **bằng English** |
| Technical | OOP, DSA, SQL, web fundamentals, design | CTCI Ch.7 + Ch.9 + SQL deep |
| Architecture talk | Scale DAM: assets, metadata, search | File storage + search design |

Official note (từ OL): challenge 60 phút, 2 coding problems; .NET giúp nhưng không bắt buộc nếu giỏi 1 backend language và sẵn sàng học.

---

## 2. Timeline 6–8 tuần

### Tuần 1–2 — Timed coding + OOP

**LeetCode (NeetCode) — mode “OL challenge”:**
- Arrays & Hashing, Two Pointers, Sliding Window, Stack, Binary Search
- **Mỗi tuần ≥ 2 session: đúng 2 bài / 60'** (giống challenge)
- Ưu tiên bài “clean code + edge cases” hơn bài trick cực khó

**CTCI:** Ch.1–3; bắt đầu **Ch.7 Object-Oriented Design**

**OOP / design (OL-heavy):**
- Encapsulation, inheritance vs composition
- SOLID đủ để design module Upload / Asset / Permission
- Class design: `Asset`, `Metadata`, `Folder`, `Permission`, `Version`

**English (song song mỗi ngày 20–30'):**
- Giải thích solution **bằng tiếng Anh** sau mỗi bài (record giọng)
- Vocab: scalability, trade-off, maintainability, edge case, throughput

**Deliverable:** 4 timed sessions logged (pass/fail, bài nào chậm)

---

### Tuần 3–4 — Trees/Graphs + SQL + DAM domain

**LeetCode:**
- Linked List, Trees, Heap, Graphs BFS/DFS
- Intervals (merge — hay gặp practical)
- Tiếp tục timed 2/60' × 2–3 buổi

**CTCI:** Ch.4, Ch.10; đọc nhẹ Ch.11 Testing

**SQL (must cho OL):**
- JOIN, GROUP BY, window functions cơ bản
- Index: khi nào giúp / hại
- Normalization vs denormalize metadata
- Transaction khi update metadata + permission

**Domain DAM (đọc & sketch):**
- Digital asset = file (blob) + metadata + permissions + versions + workflow
- Object storage (S3) vs DB metadata
- Search: Elasticsearch — inverted index overview
- Thumbnail / transcoding async pipeline

**Design sketch:** “Upload ảnh/video + lưu metadata + search theo tag”

**Networking:**
- HTTP multipart upload, resumable upload overview
- CDN cho asset delivery
- Signed URL (security)

---

### Tuần 5–6 — DP + Scalability DAM + English mock

**LeetCode:**
- 1-D DP, Greedy, Backtracking selective
- Review toàn bộ Easy–Medium đã sai
- Challenge simulation: 3 buổi full 2/60'

**CTCI:** **Ch.9 System Design & Scalability** — map sang DAM

**Scalability / Reliability (OL-flavored):**
- Hot assets / cache metadata at edge (OL có nói edge metadata caching)
- Large file upload: chunking, retry, checksum
- Search index lag (eventual) vs strong consistency cho permission
- Workflow / RPA: async jobs, idempotent workers
- Multi-tenant Fortune 100: isolation, audit, compliance mindset

**Reliability checklist:**
- Corrupt upload → checksum + quarantine
- Partial failure: file lên S3 nhưng metadata fail → compensating / cleanup
- AuthZ trên từng asset

**English behavioral (must):**
- 6 STAR stories viết sẵn + luyện nói
- Why OL / why DAM / learning .NET if coming from Java
- Conflict, ownership, thoroughness (cultural keywords OL hay nhấn: humility, resilience, thoroughness)

**Mock:**
- 2 coding timed  
- 1 OOP design (English)  
- 1 DAM system sketch (English)  
- 1 HR mock English 30'

---

### Tuần 7–8 (buffer) — Stack bridge + polish

- Nếu chưa biết .NET: skim C# syntax + async/await vs Java (đủ nói “learn fast”)
- Elasticsearch: document vs row, text search basics
- AWS: S3, IAM overview
- Ôn SQL viết tay trên giấy
- Final: 2 challenge simulations + 1 full mock loop

---

## 3. NeetCode priority cho OL

| Must (challenge) | Nice | Later |
|------------------|------|-------|
| Arrays, Hash, Two Pointers, Sliding Window | Backtracking | Heavy Graph algorithms |
| Stack, Binary Search, Linked List | Tries | Advanced DP 2D |
| Trees, BFS/DFS, Heap | Bit | |
| Intervals, 1-D DP | | |

**Khác MoMo/Axon:** tốc độ + code sạch trong 60' quan trọng hơn độ khó “Hard”.

Gợi ý pool trước challenge: ~50–70 bài, trong đó ≥15 buổi timed.

---

## 4. CTCI focus OL

1. **Ch.7 OOD** — luyện design classes/modules (rất hợp product company)  
2. **Ch.9** — scale storage + read path  
3. Ch.1–4, Ch.8 — phục vụ coding challenge  
4. Ch.11 — unit test mindset (OL JD nhấn unit tests / complete features)

---

## 5. Checklist kiến thức “OL / DAM-flavored”

### Scalability
- [ ] Tách blob storage vs metadata DB
- [ ] Search index không nằm trên DB chính
- [ ] Cache metadata / permission
- [ ] Async pipeline: transcode, AI tagging
- [ ] Scale read (CDN) vs write (upload burst)

### Reliability
- [ ] Checksum / integrity file
- [ ] Retry upload chunk
- [ ] Job queue failure & poison message
- [ ] Audit trail ai xem/sửa asset

### CS
- [ ] OOP design rõ ràng trên whiteboard
- [ ] Tree/Graph cho folder hierarchy & permissions
- [ ] Hashing cho dedup content (overview)

### Networking
- [ ] HTTPS + signed URL
- [ ] Upload lớn trên mạng không ổn định
- [ ] CDN caching headers overview

### English
- [ ] Giải thích algorithm bằng English
- [ ] HR answers trôi chảy 5–8 phút/topic
- [ ] Hỏi lại clarifications lịch sự khi interview

### LeetCode
- [ ] 2 Medium trong 60' — ổn định ≥ 70% sessions
- [ ] Code có test cases tự nghĩ

---

## 6. Bài design / câu hỏi luyện (OL)

**Coding challenge style:** string/array manipulation, hashing, two pointers, tree easy–medium, BFS, interval merge, simple DP.

**OOD:**
- Design permission model (user, group, folder, asset)
- Versioning khi replace file

**System:**
- Design DAM upload + search
- “Hàng triệu video request kèm auth” — cache ở đâu, invalidate thế nào?
- Metadata enrichment bằng AI — sync hay async?

**Behavioral (English prompts):**
- Tell me about a feature you owned end-to-end  
- Describe a time you were thorough under deadline pressure  
- How do you learn a new stack quickly?

---

## 7. Lịch tuần mẫu (OL)

| Slot | Việc |
|------|------|
| 4×/tuần × 60–90' | NeetCode (ít nhất 2 session timed 2/60') |
| 3×/tuần × 25' | English explain solution / STAR |
| 2×/tuần × 45' | SQL + OOP/DAM design |
| Cuối tuần | Full challenge simulation + journal |

---

## 8. Definition of Ready

- [ ] Timed: 2 bài / 60' đạt ổn định  
- [ ] Giải thích OOP design Asset/Permission bằng English  
- [ ] Sketch được DAM upload + metadata + search  
- [ ] SQL tự tin (join, index, transaction)  
- [ ] 6 STAR stories English  
- [ ] Hiểu product Orange Logic / DAM đủ để trả lời “Why us?”  

→ Apply / làm challenge khi checklist xanh.
