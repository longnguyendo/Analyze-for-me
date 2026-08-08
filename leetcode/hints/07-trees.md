# Hints — Trees (#134–168)

| # | LC | Hint |
|---|-----|------|
| 134 | 226 | Swap left/right đệ quy hoặc BFS |
| 135 | 104 | 1 + max(left,right) |
| 136 | 543 | DFS trả height; update diameter = L+R |
| 137 | 110 | DFS trả height; −1 nếu lệch >1 |
| 138 | 100 | So val + đệ quy 2 nhánh |
| 139 | 572 | Với mỗi node check sameTree |
| 140 | 235 | BST: đi theo khoảng p,q |
| 141 | 236 | Postorder: tìm 2 phía; cả 2 ≠null → root |
| 142 | 102 | BFS queue theo level |
| 143 | 107 | BFS rồi reverse kết quả |
| 144 | 103 | BFS + đảo chiều từng level |
| 145 | 199 | BFS: node cuối mỗi level |
| 146 | 98 | DFS kèm bound (low, high) |
| 147 | 230 | Inorder BST → phần tử thứ k |
| 148 | 105 | Preorder root; tách inorder bằng map index |
| 149 | 106 | Postorder root cuối; tách inorder |
| 150 | 124 | DFS trả max path xuống; update max qua node |
| 151 | 297 | Preorder + null marker; hoặc BFS serialize |
| 152 | 144 | Stack iterative preorder |
| 153 | 94 | Stack inorder classic |
| 154 | 145 | 2 stack hoặc reverse preorder biến thể |
| 155 | 101 | Mirror: so left.left với right.right |
| 156 | 112 | DFS trừ remaining |
| 157 | 113 | DFS path list + backtrack |
| 158 | 437 | Prefix sum trên path + map |
| 159 | 129 | DFS tích số `cur*10+val` |
| 160 | 257 | DFS nối path string |
| 161 | 222 | So height trái/phải → công thức complete tree |
| 162 | 116 | BFS hoặc nối next bằng con trỏ level |
| 163 | 117 | BFS level (không perfect) |
| 164 | 337 | DFS trả (rob, notRob) |
| 165 | 968 | DFS 3 state: có camera / covered / need |
| 166 | 662 | BFS với index như heap (2*i, 2*i+1) |
| 167 | 863 | Build parent map; BFS từ target khoảng K |
| 168 | 314 | BFS + cột index; TreeMap theo cột |
