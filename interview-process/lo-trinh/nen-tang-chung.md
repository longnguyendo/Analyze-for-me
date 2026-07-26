# Nền tảng chung — NeetCode + CTCI + Systems

Dùng chung cho MoMo / OL / Axon. Mỗi công ty sẽ **nhấn mạnh khác nhau** ở phần domain; phần này là skeleton bắt buộc.

---

## 1. LeetCode theo NeetCode

### Mục tiêu cho SE 1.5 YOE

- Hoàn thành **NeetCode 75** (core) → mở rộng **NeetCode 150** nếu target Axon/MoMo.
- Pattern > số lượng: mỗi pattern làm 5–8 bài, giải thích được trade-off.
- Mục tiêu tốc độ: Easy ~15', Medium ~25–35', luôn nói được complexity.

### Thứ tự học (NeetCode Roadmap)

| # | Topic | CTCI map | Priority SE 1.5 |
|---|--------|----------|-----------------|
| 1 | Arrays & Hashing | Ch.1 | Must |
| 2 | Two Pointers | Ch.1 | Must |
| 3 | Sliding Window | Ch.1 | Must |
| 4 | Stack | Ch.3 | Must |
| 5 | Binary Search | Ch.10 | Must |
| 6 | Linked List | Ch.2 | Must |
| 7 | Trees | Ch.4 | Must |
| 8 | Tries | Ch.4 | Nice |
| 9 | Heap / Priority Queue | Ch.3–4 | Must |
| 10 | Backtracking | Ch.8 | Medium |
| 11 | Graphs (BFS/DFS) | Ch.4 | Must |
| 12 | Advanced Graphs | Ch.4 | Axon/MoMo |
| 13 | 1-D DP | Ch.8 | Must |
| 14 | 2-D DP | Ch.8 | Axon+ |
| 15 | Greedy | — | Medium |
| 16 | Intervals | — | Must |
| 17 | Math & Geometry | Ch.6 | Medium |
| 18 | Bit Manipulation | Ch.5 | Axon / nice MoMo |

### Ritme luyện hàng ngày

- **5 ngày/tuần × 1–2 bài** (1 Medium hoặc 2 Easy).
- 1 ngày/tuần: **revision** — làm lại bài cũ không nhìn solution.
- 1 ngày/tuần: **timed contest-style** (2 bài / 60') — đặc biệt quan trọng cho OL.

### Cách giải (CTCI style)

1. Clarify input/output, constraints, examples.
2. Brute force trước → optimize.
3. Nói time/space trước khi code.
4. Test edge cases (empty, overflow, duplicates).
5. Sau khi AC: viết 3–5 dòng “pattern notes”.

---

## 2. Cracking the Coding Interview — chapters ưu tiên

| Chapter | Chủ đề | Khi nào đọc |
|---------|--------|-------------|
| Ch.1–4 | Arrays, LL, Stack/Queue, Trees/Graphs | Tuần 1–4 song song NeetCode |
| Ch.5 | Bit Manipulation | Trước vòng Axon CS |
| Ch.7 | Object-Oriented Design | Trước OL / MoMo design |
| Ch.8 | Recursion & DP | Tuần 4–7 |
| Ch.9 | **System Design & Scalability** | Bắt buộc cả 3 công ty |
| Ch.10 | Sorting & Searching | Tuần 2–3 |
| Ch.11 | Testing | Behavioral + quality talk |
| Big O (intro) | Complexity | Ngày 1, review liên tục |

**Cách đọc CTCI:** không đọc hết như sách giáo khoa. Mỗi chapter: đọc framework → làm 4–6 bài interview questions → map sang NeetCode pattern tương đương.

---

## 3. Scalability (CTCI Ch.9 + thực chiến)

Hiểu và giải thích được (whiteboard / verbal):

| Concept | Câu hỏi tự kiểm |
|---------|-----------------|
| Vertical vs horizontal scale | Khi nào scale up vs out? |
| Load balancer | L4 vs L7, sticky session trade-off |
| Caching | Cache-aside, TTL, stampede, invalidation |
| DB scale | Index, read replica, sharding, when NoSQL |
| Async | Queue (Kafka/Rabbit), backpressure |
| CDN / object storage | Static vs hot path |
| CAP / consistency | Strong vs eventual — ví dụ thanh toán vs feed |

**Bài design tối thiểu (SE 1.5):**

1. URL shortener  
2. Rate limiter  
3. Feed / notification (async)  
4. File upload + metadata (gần OL/Axon)  
5. Payment transfer (idempotent) — gần MoMo  

Với 1.5 YOE: **không cần** design toàn bộ Netflix. Cần: requirements → API → data model → bottlenecks → 1–2 scale levers → failure modes.

---

## 4. Reliability

| Chủ đề | Bạn phải nói được |
|--------|-------------------|
| Idempotency | Retry an toàn khi timeout |
| Timeouts / retries / backoff | Tránh retry storm |
| Circuit breaker / bulkhead | Cô lập failure |
| Health check / graceful degradation | Fail soft |
| Observability | Logs, metrics, traces — debug production |
| Transactions | ACID vs saga / outbox (mức overview) |
| Data integrity | Checksum, versioning, audit trail |

Checklist tự hỏi sau mỗi design: *“Nếu 1 service chết / DB chậm / network partition thì user thấy gì?”*

---

## 5. Computer Science fundamentals

| Area | Topics tối thiểu |
|------|------------------|
| Data structures | Array, hash, heap, tree, graph — khi dùng cái nào |
| Algorithms | Sorting, searching, BFS/DFS, Dijkstra overview |
| OS | Process vs thread, context switch, mutex/lock, deadlock, virtual memory, page cache |
| Concurrency | Race, atomicity, thread pool, async I/O |
| Memory | Stack vs heap, GC basics (Java/.NET) |
| Complexity | Amortized, worst vs average |

Axon sẽ đào sâu hơn; MoMo/OL hỏi ở mức “hiểu đủ để debug & design”.

---

## 6. Networking

| Topic | Level cần |
|-------|-----------|
| OSI / TCP vs UDP | Khi dùng UDP, TCP handshake, TIME_WAIT overview |
| HTTP/1.1 vs HTTP/2 / HTTPS | TLS handshake high-level, status codes |
| DNS | Resolve path, TTL |
| REST vs gRPC | Trade-off |
| WebSocket | Khi nào realtime |
| Latency vs bandwidth | Buffer, Nagle (overview cho Axon) |
| Security basics | AuthN/Z, JWT, CORS, SQL injection |

---

## 7. Behavioral (CTCI + STAR)

Chuẩn bị 6–8 stories (STAR):

1. Conflict trong team  
2. Bug production / on-call  
3. Trade-off kỹ thuật bạn chọn  
4. Học skill mới nhanh  
5. Miss deadline / lesson  
6. Ownership feature end-to-end  

Axon & OL: **English** cho behavioral / HR. MoMo: CV English + technical chủ yếu tiếng Việt/Anh mix tùy interviewer.

---

## 8. Weekly template (dùng lại)

| Ngày | Focus |
|------|--------|
| Mon–Tue | NeetCode topic mới (2–3 bài) |
| Wed | CS / Networking notes + flashcards |
| Thu | NeetCode + 1 CTCI question |
| Fri | System design / reliability sketch (45–60') |
| Sat | Timed coding (60') + review sai |
| Sun | Mock (coding hoặc behavioral) + journal |

---

## Resources nhanh

- NeetCode roadmap: https://neetcode.io/roadmap  
- CTCI (Gayle Laakmann McDowell) — bản bạn đang có  
- System Design Primer (GitHub) — đọc có chọn lọc  
- Company-specific: xem file lộ trình riêng
