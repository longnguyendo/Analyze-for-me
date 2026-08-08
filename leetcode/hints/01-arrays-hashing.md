# Hints — Arrays & Hashing (#1–35)

Hint ngắn: định hướng pattern, **không** full code.

| # | LC | Hint |
|---|-----|------|
| 1 | 217 | HashSet — gặp số đã thấy → true |
| 2 | 242 | Đếm tần suất 26 chữ (array[26]) hoặc sort rồi so |
| 3 | 1 | HashMap value→index; với mỗi x tìm target−x |
| 4 | 49 | Key = sorted string hoặc đếm frequency tuple |
| 5 | 347 | Đếm freq → bucket sort theo freq hoặc heap size k |
| 6 | 238 | Prefix product trái × suffix phải; O(1) extra nếu cẩn thận |
| 7 | 36 | Set cho hàng/cột/box `r/3,c/3` |
| 8 | 128 | Set; chỉ bắt đầu đếm khi `num-1` không có |
| 9 | 271 | Encode độ dài + delimiter trước mỗi string |
| 10 | 560 | Prefix sum + map đếm prefix; tìm `sum−k` |
| 11 | 523 | Prefix % k; cùng modulo → đoạn chia hết k (len≥2) |
| 12 | 525 | Map 0→−1, 1→+1; gặp cùng running sum → đoạn cân bằng |
| 13 | 41 | Đặt mỗi số về index đúng `nums[i]=i+1` (cyclic sort) |
| 14 | 287 | Floyd cycle (tortoise/hare) trên mảng như linked list |
| 15 | 442 | Đánh dấu bằng cách đảo dấu tại index `abs(x)-1` |
| 16 | 448 | Tương tự mark index; số nào index chưa mark → missing |
| 17 | 136 | XOR toàn bộ — cặp triệt tiêu |
| 18 | 169 | Boyer–Moore voting hoặc đếm |
| 19 | 229 | Extended Boyer–Moore: tối đa 2 ứng viên |
| 20 | 75 | Dutch national flag: 3 con trỏ low/mid/high |
| 21 | 283 | Two pointer ghi số ≠0 về đầu, rồi fill 0 |
| 22 | 189 | Reverse toàn mảng → reverse 2 đoạn k |
| 23 | 88 | Merge từ cuối mảng (tránh ghi đè) |
| 24 | 26 | Slow pointer ghi giá trị unique |
| 25 | 27 | Slow pointer ghi giá trị ≠ val |
| 26 | 80 | Cho phép tối đa 2; so với `nums[slow-2]` |
| 27 | 118 | Mỗi hàng: cạnh =1, giữa = tổng 2 số trên |
| 28 | 119 | Tối ưu O(rowIndex) bằng 1 mảng cập nhật từ phải |
| 29 | 54 | 4 biên top/bottom/left/right thu hẹp dần |
| 30 | 59 | Cùng 4 biên, điền số tăng dần |
| 31 | 48 | Transpose rồi reverse từng hàng (hoặc layer xoay) |
| 32 | 73 | Dùng hàng 0 / cột 0 làm marker (O(1) space) |
| 33 | 289 | Encode state tạm bằng số 2-bit rồi decode |
| 34 | 566 | Map index phẳng `i*c+j` sang shape mới |
| 35 | 766 | So `matrix[i][j] == matrix[i-1][j-1]` |
