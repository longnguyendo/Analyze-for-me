# Hints — Greedy / Intervals / Math / Bit / Design (#297–325)

| # | LC | Hint |
|---|-----|------|
| 297 | 55 | Track farthest reach |
| 298 | 45 | BFS-on-array: end/farthest từng “jump level” |
| 299 | 53 | Kadane |
| 300 | 134 | Nếu total gas≥cost; start tại điểm tank không âm |
| 301 | 846 | Đếm + luôn lấy consecutive từ min |
| 302 | 1899 | Chỉ merge triplet ≤ target; cover từng vị trí |
| 303 | 763 | Last index mỗi chữ; greedy cut |
| 304 | 678 | 2 pass hoặc balance range low/high với `*` |
| 305 | 56 | Sort start; merge nếu overlap |
| 306 | 57 | Chèn + merge overlapping |
| 307 | 435 | Sort end; greedy giữ sớm kết thúc |
| 308 | 252 | Sort start; check overlap kế |
| 309 | 253 | Min-heap end times; hoặc sweep +/− |
| 310 | 1851 | Sort + min-heap intervals theo size |
| 311 | 202 | Floyd cycle trên next happy |
| 312 | 66 | Cộng từ cuối; carry |
| 313 | 50 | Ôn binary exponent |
| 314 | 43 | Nhân nhân như giấy; mảng digit |
| 315 | 48 | Ôn transpose+reverse |
| 316 | 54 | Ôn 4 biên |
| 317 | 73 | Ôn marker hàng/cột 0 |
| 318 | 201 | Dịch phải đến bằng nhau (common prefix bits) |
| 319 | 371 | XOR + carry<<1 lặp |
| 320 | 338 | dp[i]=dp[i>>1]+(i&1) |
| 321 | 191 | Brian Kernighan `n&=n-1` hoặc đếm bit |
| 322 | 190 | Dịch bit từng vị trí |
| 323 | 268 | XOR 0..n với nums; hoặc công thức sum |
| 324 | 146 | HashMap + Doubly Linked List |
| 325 | 380 | HashMap value→index + swap-remove mảng |

## Pattern cheatsheet nhanh

| Pattern | Nhận diện |
|---------|-----------|
| Greedy jump | “có thể tới cuối / số bước tối thiểu” |
| Interval | overlap, meeting rooms, merge |
| Bit | không dùng +/− *, đếm bit, range AND |
| Design O(1) | kết hợp HashMap + cấu trúc phụ |
