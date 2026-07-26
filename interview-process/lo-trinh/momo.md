# Lộ trình MoMo — SE ~1.5 YOE

**Công ty:** MoMo (M_Service) — fintech / e-wallet  
**Stack thường gặp:** Java (Spring), SQL (Oracle/PostgreSQL), Redis, Kafka/RabbitMQ, microservices  
**Quy trình điển hình:** Screening (CV English) → Online test → Interview (resume + fundamentals + coding/design)

> Mục tiêu: thể hiện bạn **hiểu hệ thống thanh toán quy mô lớn** — consistency, idempotency, throughput — không chỉ CRUD.

Xem nền tảng chung: [nen-tang-chung.md](./nen-tang-chung.md)

---

## 1. Map vòng phỏng vấn → cần học gì

| Vòng | Họ đánh giá | Prep chính |
|------|-------------|------------|
| CV screening | English CV, transcript, fit | CV nhấn Java, SQL, scale metrics |
| Online test | DSA + logic / practical | NeetCode Easy–Medium timed |
| Technical interview | Project deep-dive, Java/SQL, DSA, design nhỏ | CTCI + system notes fintech |
| (Có thể) System / architecture | Scale, cache, queue, consistency | CTCI Ch.9 + payment patterns |

---

## 2. Timeline 8–10 tuần

### Tuần 1–2 — Foundation + Java mindset

**LeetCode (NeetCode):**
- Arrays & Hashing, Two Pointers, Sliding Window, Stack
- 8–10 bài; ưu tiên Medium

**CTCI:** Ch.1, Big O; bắt đầu Ch.10 (search/sort)

**CS / Java (MoMo-heavy):**
- Collections internals (HashMap, ArrayList, ConcurrentHashMap overview)
- OOP: SOLID đủ để giải thích design trong project
- SQL: index, EXPLAIN mindset, transaction isolation levels (READ COMMITTED vs REPEATABLE READ)

**Scalability / Reliability intro:**
- Cache-aside với Redis
- Idempotent API (key quan trọng cho payment)

**Deliverable tuần 2:** 1 trang notes “Project của tôi → bottlenecks & cách scale”

---

### Tuần 3–4 — Graphs/Trees + DB + Messaging

**LeetCode:**
- Binary Search, Linked List, Trees, Heap
- Graphs BFS/DFS (5–6 bài)

**CTCI:** Ch.2–4

**Domain MoMo:**
- Message queue: at-least-once vs exactly-once (thực tế: idempotent consumer)
- Kafka/Rabbit: khi nào dùng, ordering, DLQ
- Redis: cache, distributed lock (risks), rate limit đơn giản

**Networking:**
- HTTP status, REST design, timeout giữa services
- TCP basics (đủ để nói connection pool / keep-alive)

**Design sketch:** Rate limiter **hoặc** Notification service (async)

---

### Tuần 5–6 — DP + Consistency + Payment design

**LeetCode:**
- Intervals, Greedy, 1-D DP (House Robber, Climbing Stairs, Coin Change…)
- Ôn lại Arrays/Hashing (online test hay ra)

**CTCI:** Ch.8 (một phần), **Ch.9 System Design & Scalability** (đọc kỹ)

**Reliability / Scalability (core MoMo):**
- Money transfer flow: validate → reserve/hold → commit → notify
- Idempotency key, exactly-once *effect*
- Strong consistency chỗ nào (số dư) vs eventual (notification, analytics)
- Outbox / dual-write problem (overview)
- Failure: timeout ngân hàng đối tác → retry + reconcile

**Design sketch (must):** “Thiết kế API chuyển tiền nội bộ MoMo”  
Clarify: correctness > latency; audit log; concurrency trên balance

**Networking + Security:**
- TLS overview, auth giữa services
- Không log PII/số dư nhạy cảm

---

### Tuần 7–8 — Mock + Online test mode + Java concurrency

**LeetCode:**
- NeetCode 75: cover gaps; timed 2 bài / 60' × 3 buổi
- Bit Manipulation cơ bản (nice-to-have)

**Java concurrency (phỏng vấn hay hỏi):**
- Thread vs ExecutorService
- synchronized / Lock, volatile overview
- Race trên shared balance → DB transaction / optimistic locking

**CS:**
- Process vs thread
- GC basics (stop-the-world overview — không cần CMS vs G1 chi tiết)

**Mock:**
- 3 coding mocks (talk while coding)
- 2 project deep-dives (15' explain + follow-up scale/failure)
- 1 payment / cache design

---

### Tuần 9–10 (buffer) — Polish theo JD

- Đọc JD team apply (Gift, Payment, Credit…) → chỉnh story
- Ôn SQL joins, indexing, deadlock
- Review tất cả Medium đã sai
- Behavioral STAR (ownership, production bug, trade-off)

---

## 3. NeetCode priority cho MoMo

| Must | Medium priority | Skip / later |
|------|-----------------|--------------|
| Arrays, Hash, Two Pointers, Sliding Window | Backtracking | Advanced Graph (unless time) |
| Stack, Binary Search, Trees | 2-D DP | Pure Math puzzles |
| BFS/DFS, Heap, Intervals | Tries | |
| 1-D DP | Bit | |

**Số lượng gợi ý trước interview:** ~60–80 bài chất lượng (75 NeetCode là đủ nếu nắm pattern).

---

## 4. CTCI focus MoMo

1. **Ch.9** — scalability patterns (đọc + tự áp vào ví dụ ví điện tử)  
2. Ch.1–4, Ch.8 — song song coding  
3. Ch.7 OOD — design class cho Wallet / Transaction (LLD nhẹ)  
4. Ch.11 Testing — nói về unit/integration cho money flow  

---

## 5. Checklist kiến thức “MoMo-flavored”

### Scalability
- [ ] Horizontal scale stateless API + sticky khi nào cần
- [ ] Read replica vs cache
- [ ] Partition key cho transaction history
- [ ] Hot key (user VIP balance) — vấn đề & mitigation

### Reliability
- [ ] Idempotent payment API
- [ ] Retry + backoff + jitter
- [ ] Reconciliation job
- [ ] Circuit breaker khi partner chậm

### CS
- [ ] HashMap complexity & collision overview
- [ ] Index B-Tree mindset
- [ ] Transaction isolation
- [ ] Thread safety basics

### Networking
- [ ] REST error handling
- [ ] Timeout / connection pool
- [ ] HTTPS & token auth overview

### LeetCode
- [ ] NeetCode 75 ≥ 80% topics must
- [ ] 5 buổi timed online-test style

---

## 6. Câu hỏi / bài hay gặp (luyện nói)

**Coding:** Two Sum variants, anagram, sliding window substring, binary search, tree traversal, BFS shortest path, merge intervals, coin change.

**System / conceptual:**
- Tại sao không trừ tiền chỉ bằng `UPDATE balance = balance - x`?
- Cache số dư được không? Khi nào invalidate?
- Kafka consumer crash giữa chừng thì sao?
- Phân biệt at-least-once và “xử lý đúng một lần về mặt nghiệp vụ”

**Project:**
- Metric: QPS, latency p99, data size
- Bottleneck từng gặp và cách đo

---

## 7. Lịch tuần mẫu (MoMo)

| Slot | Việc |
|------|------|
| Sáng / 90' | 1–2 NeetCode + notes pattern |
| Tối 45' | Java/SQL/CS flashcards hoặc CTCI |
| Cuối tuần 90' | Design payment/cache **hoặc** timed test |
| 1×/tuần | Mock 45–60' với bạn / tự record |

---

## 8. Definition of Ready (sẵn sàng apply / interview)

- [ ] NeetCode 75: hầu hết Must topics làm được không nhìn lời giải  
- [ ] Giải thích được 1 project end-to-end + 3 failure scenarios  
- [ ] Whiteboard được transfer tiền + idempotency  
- [ ] SQL: viết được query có index rationale  
- [ ] Online test: 2 Medium / 60' ổn định  
- [ ] CV English sạch, số liệu cụ thể  

Khi xong checklist → book mock cuối → apply / confirm lịch MoMo.
