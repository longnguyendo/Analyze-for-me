# Hints — Sliding Window (#56–73)

| # | LC | Hint |
|---|-----|------|
| 56 | 121 | Track min price phía trái; max profit = price−min |
| 57 | 3 | Window + last index map; co left khi trùng |
| 58 | 424 | Window; `len − maxFreq ≤ k` thì hợp lệ |
| 59 | 567 | Window cố định len(s1); so frequency map |
| 60 | 76 | Expand phải đến đủ need; co trái tối thiểu |
| 61 | 209 | Expand đến sum≥target; co trái lấy min len |
| 62 | 904 | At most 2 loại; map đếm loại trong window |
| 63 | 1004 | Co khi số 0 trong window > k |
| 64 | 487 | Giống 1004 với k=1 |
| 65 | 159 | At most 2 distinct chars |
| 66 | 340 | At most K distinct — map size ≤ k |
| 67 | 438 | Window cố định; so hash/freq với p |
| 68 | 30 | Window theo wordLen; đếm từ khớp |
| 69 | 239 | Monotonic deque giảm dần (index) |
| 70 | 480 | 2 heap / policy dựa multiset — khó; luyện sau |
| 71 | 643 | Window cố định k; track sum |
| 72 | 1456 | Window k; đếm nguyên âm |
| 73 | 187 | Window 10; hash/set các substring đã thấy |
