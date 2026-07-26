# Lộ trình Axon — SE ~1.5 YOE

**Công ty:** Axon — public safety / evidence tech (bodycam, evidence management); bar kỹ thuật **cao** tại VN  
**Nhấn mạnh:** CS fundamentals sâu (OS, networking, concurrency), LeetCode medium+, system thinking, **English**  
**Quy trình điển hình (VN experiences):**  
1. HR screen (English)  
2. Tech basics + coding (project deep-dive → DB/OS/Network → Medium coding)  
3. Technical deep loop (~4 sessions × 1h): CS fundamentals · Coding + follow-ups · Coding + performance/threads/network · Behavioral  
4. (Biến thể global) phone screen / design / thêm coding — chuẩn bị rộng hơn một chút

> Mục tiêu: không chỉ “AC LeetCode”, mà **giải thích được CPU, memory, threads, TCP** khi họ xoay follow-up. Với 1.5 YOE vẫn pass được nếu CS chắc (đã có case ~2 YOE pass).

Xem nền tảng chung: [nen-tang-chung.md](./nen-tang-chung.md)

---

## 1. Map vòng phỏng vấn → cần học gì

| Vòng / session | Họ đào | Prep |
|----------------|--------|------|
| HR | English, motivation, career | STAR English + Why Axon |
| Tech screen | Project → DB/OS/Network → Medium DSA | CTCI + CS notes + NeetCode |
| CS Fundamentals | OS scheduling, memory, cache, DS sâu | OS + CS course refresh |
| Coding + follow-up | Medium + biến thể + cấu trúc khác | NeetCode 75→150, CTCI |
| Coding + systems | Threads, CPU, parallel, TCP/UDP, buffers | Concurrency + Networking labs |
| Behavioral | Conflict, quality vs speed, teamwork | STAR khó — không “nghỉ” |
| System design (nếu có) | Upload video, logging, search, custody | Reliability + large file + audit |

---

## 2. Timeline 10–14 tuần

### Tuần 1–3 — NeetCode foundation + CS warm-up

**LeetCode:**
- Arrays & Hashing → Two Pointers → Sliding Window → Stack → Binary Search → Linked List
- Trees + Heap
- Mục tiêu: pattern vững, bắt đầu **nói English** khi giải

**CTCI:** Ch.1–3, Big O; notes mỗi pattern

**CS daily (45'/ngày):**
- Process vs Thread vs Coroutine
- User vs kernel mode (overview)
- CPU cache (L1/L2), locality — tại sao array nhanh hơn linked list thực tế
- Virtual memory, page fault (high-level)

**Networking warm-up:**
- TCP handshake, UDP use cases
- HTTP vs raw TCP

**Deliverable tuần 3:** cheatsheet 2 trang “OS + Network for interviews”

---

### Tuần 4–6 — Graphs, DP, concurrency coding

**LeetCode:**
- Graphs BFS/DFS + vài topological / shortest path overview
- 1-D DP full set NeetCode; bắt đầu 2-D DP selective
- Backtracking, Intervals, Greedy
- **Follow-up drills:** mỗi bài hỏi thêm “đổi constraint thì DS nào?”

**CTCI:** Ch.4, Ch.8, Ch.5 (Bit — Axon hay liên quan low-level thinking)

**Concurrency (cực quan trọng Axon):**
- Race condition, mutex, deadlock (4 conditions)
- Thread pool, work stealing overview
- Parallelize CPU-bound vs I/O-bound
- Bài tập tư duy: “4 cores — chia task thế nào? shared state?”

**Reliability:**
- Exactly-once effect, retries
- Backpressure

**Mock:** 1 coding/week (English) + 1 CS oral/week

---

### Tuần 7–9 — Deep CS + Networking + System sketches

**LeetCode:**
- Hoàn thiện NeetCode 75; đẩy thêm bài Medium tagged hard-followup
- Advanced: Union-Find, Dijkstra overview (không cần expert)
- Timed + **follow-up only sessions** (30' optimize / variant)

**CTCI:** **Ch.9** kỹ; Ch.7 OOD; Ch.10

**OS sâu (session CS style):**
- Scheduling (RR, CFS idea)
- Context switch cost
- Mutex vs spinlock (khi nào)
- Memory allocator / fragmentation overview
- Disk I/O vs page cache

**Networking sâu:**
- TCP: congestion vs flow control (phân biệt được)
- Head-of-line blocking
- Buffer size & latency
- TLS placement
- gRPC / HTTP/2 multiplexing overview

**Scalability + Axon domain:**
- Large video upload trên mạng xấu (chunk, resume, retry)
- Object storage + metadata DB
- Chain of custody / tamper-evident audit (hash chain overview)
- Search / indexing evidence metadata
- Device logging → upload → query trong vài phút (pipeline)

**Design sketches (3):**
1. Resumable video upload + integrity  
2. Device log ingestion  
3. Rate-limited evidence search API  

---

### Tuần 10–12 — Full mocks (Axon loop simulation)

**Giả lập vòng 3 (4 × 60', nghỉ ngắn hoặc không — tập stamina):**

| Session | Nội dung luyện |
|---------|----------------|
| 1 | CS oral: OS + DS + memory (chỉ nói, ít code) |
| 2 | Coding Medium + 2–3 follow-ups |
| 3 | Coding + “dùng 4 cores” + TCP/buffer questions |
| 4 | Behavioral English (dồn dập) |

Lặp simulation này **2–3 lần** trong 3 tuần.

**LeetCode:** revision list sai; 1 Hard optional nếu còn sức (không bắt buộc 1.5 YOE).

**English:** HR + behavioral mỗi ngày 20'

---

### Tuần 13–14 (buffer)

- Weak topic surgery (thường: DP follow-up, OS scheduling, TCP)
- Project deep-dive: đo được latency, concurrency bugs đã fix
- Why Axon / public safety impact — chân thật, English
- Sleep & logistics trước interview loop

---

## 3. NeetCode priority cho Axon

| Must | Strongly recommended | If time |
|------|----------------------|---------|
| Full NeetCode 75 | NeetCode 150 (select) | Hard DP |
| Graphs + Trees sâu | Bit Manipulation | Advanced Graph |
| 1-D + basic 2-D DP | Heap puzzles | |
| Follow-up variants | Design-coding hybrids (LRU, Underground System style) | |

**Khác biệt:** Axon đánh **follow-up + performance reasoning** nặng hơn số lượng AC.

---

## 4. CTCI focus Axon

1. Ch.1–5, Ch.8 — coding + bit  
2. **Ch.9** — scale + reliability language  
3. Phần intro OS/complexity — kết hợp sách OS khác nếu cần (Operating Systems Concepts overview / blog)  
4. Behavioral chapters / interview soft skills — chuẩn bị session 4  

---

## 5. Checklist kiến thức “Axon-flavored”

### Scalability
- [ ] Ingest throughput (devices → cloud)
- [ ] Storage tiering (hot metadata / cold video)
- [ ] Search vs transactional DB
- [ ] Horizontal workers cho transcode/scan

### Reliability
- [ ] Checksum / tamper-evident logs
- [ ] Resumable upload trên mạng drop
- [ ] At-least-once ingestion + dedup
- [ ] Audit: ai access evidence khi nào

### CS (must pass oral)
- [ ] Threads, locks, deadlock examples
- [ ] Scheduling & context switch
- [ ] Virtual memory & cache locality
- [ ] When array beats pointer structures
- [ ] Complexity + real hardware caveats

### Networking (must)
- [ ] TCP vs UDP với ví dụ
- [ ] Flow vs congestion control (high-level)
- [ ] Buffers, latency, throughput trade-off
- [ ] HTTPS / auth for evidence access

### LeetCode
- [ ] Medium ổn + follow-up 2 hướng
- [ ] Parallelism discussion trên 1 bài coding
- [ ] NeetCode 75 ≥ 90% must topics

### English
- [ ] HR 30' không kẹt ý
- [ ] Explain OS concept không đọc note
- [ ] Behavioral không “script cứng”

---

## 6. Câu hỏi drill (tự hỏi / mock)

**CS oral:**
- Mutex vs semaphore?  
- Điều kiện deadlock? Cách tránh?  
- Page fault xảy ra khi nào?  
- Tại sao BFS queue, DFS stack/recursion?  
- Cache miss ảnh hưởng latency thế nào?

**Coding follow-up:**
- Input lớn 10× — bottleneck CPU hay memory?  
- Parallelize được bước nào? Shared state?  
- Đổi online → streaming input?

**Network:**
- TCP đảm bảo gì / không đảm bảo gì ở app level?  
- Buffer nhỏ quá / lớn quá hại gì?

**Design:**
- Bodycam upload khi 3G yếu  
- Log từ triệu devices, query sau 3–5 phút  
- Không sửa được evidence đã lưu — thiết kế ra sao?

---

## 7. Lịch tuần mẫu (Axon — nặng hơn)

| Slot | Việc |
|------|------|
| 5×/tuần × 90' | NeetCode + follow-up notes (English) |
| 4×/tuần × 45' | OS / Network / Concurrency deep study |
| 1×/tuần × 60' | System design sketch (video/log/search) |
| 1×/tuần × 2–4h | Mock (coding hoặc full mini-loop) |
| Daily 20' | English STAR / explain-aloud |

---

## 8. Definition of Ready

- [ ] NeetCode 75 must topics vững + follow-up drills  
- [ ] Nói được OS + Networking 45' không collapse  
- [ ] Coding có parallelism / performance discussion  
- [ ] 3 design sketches Axon-domain  
- [ ] Behavioral English chịu được “dồn”  
- [ ] Project stories có số liệu + concurrency/failure  

→ Chỉ book loop Axon khi CS oral mock đạt “interviewer có thể đào thêm mà bạn không trống”.

---

## 9. Chiến lược nếu song song MoMo / OL

| Ưu tiên | Gợi ý |
|---------|--------|
| Axon là mục tiêu chính | Follow file này; MoMo/OL dùng như mock thật |
| OL trước (nhanh hơn) | Làm OL tuần 6–8 trong lúc Axon tuần 1–6 đang chạy |
| MoMo | Overlap Java/SQL với Axon CS; thêm payment design riêng |

**Cảnh báo:** đừng apply Axon quá sớm nếu mới chỉ grind LeetCode mà chưa drill OS/Network — đúng pattern fail vòng CS.
