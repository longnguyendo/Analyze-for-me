# Hints — Stack (#74–93)

| # | LC | Hint |
|---|-----|------|
| 74 | 20 | Push mở; gặp đóng phải match top |
| 75 | 155 | Stack cặp (val, min_so_far) |
| 76 | 150 | Gặp toán hạng push; toán tử pop 2 tính push |
| 77 | 22 | Backtrack: thêm `(` nếu còn; `)` nếu close<open |
| 78 | 739 | Monotonic stack giảm; lưu index chờ ngày nóng hơn |
| 79 | 853 | Time = (target−pos)/speed; stack fleet từ phải |
| 80 | 84 | Monotonic tăng: khi thấp hơn → tính diện tích |
| 81 | 85 | Mỗi hàng coi như histogram heights → LC84 |
| 82 | 496 | Map next greater của nums2 bằng mono stack |
| 83 | 503 | Circular: duyệt 2n với i%n |
| 84 | 901 | Stack (price, span); gộp span khi ≤ price |
| 85 | 402 | Mono tăng: pop lớn hơn khi còn k; bỏ leading 0 |
| 86 | 316 | Giống 402 + đếm còn xuất hiện sau |
| 87 | 394 | Stack số và string; gặp `]` thì expand |
| 88 | 71 | Split `/`; `..` pop; bỏ `.` rỗng |
| 89 | 227 | Sign + num; `*` `/` tính ngay với prev |
| 90 | 224 | Stack sign/result khi gặp `(` |
| 91 | 735 | Stack; xử lý va chạm âm/dương |
| 92 | 946 | Simulate push; pop khi top = next popped |
| 93 | 1249 | Pass 1 đánh `)`; pass 2 đánh `(` thừa |
