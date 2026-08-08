# Phím tắt DaVinci Resolve (hiệu quả cho edit YouTube / viral)

Áp dụng **DaVinci Resolve 18/19** trên **macOS**. Windows: thay `⌘` → `Ctrl`, `⌥` → `Alt`.  
Có thể xem/đổi: **DaVinci Resolve → Keyboard Customization**.

---

## 1. Phải thuộc lòng (top 30)

| Phím | Chức năng | Khi nào dùng |
|------|-----------|--------------|
| `Space` | Play / Stop | Duyệt timeline |
| `J` / `K` / `L` | Tua ngược / Pause / Tua tới (nhấn nhiều = nhanh hơn) | Scrub nhanh như editor chuyên |
| `←` / `→` | Lùi / tiến 1 frame | Cắt chính xác |
| `⇧←` / `⇧→` | 1 giây | Nhảy nhanh |
| `Home` / `End` | Đầu / cuối timeline | |
| `I` / `O` | Mark In / Out | Chọn đoạn xuất hoặc edit |
| `⌥X` | Clear In/Out | Xóa mark |
| `A` | Selection Mode (mũi tên) | Chọn / kéo clip |
| `B` | Blade (cắt) | Cắt tại playhead |
| `⌘B` | Razor tất cả track tại playhead | Cắt xuyên track |
| `/` | Append edit (thêm clip vào cuối) | Dựng nhanh |
| `F9` | Insert | Chèn tại playhead (đẩy clip sau) |
| `F10` | Overwrite | Đè lên timeline |
| `F11` | Replace | Thay clip |
| `F12` | Place on Top | Chồng track trên |
| `⌘Z` / `⌘⇧Z` | Undo / Redo | |
| `⌫` | Delete (để lỗ trống) | |
| `⇧⌫` | Ripple Delete (xóa + dồn) | Loại dead air |
| `⌘C` / `⌘V` | Copy / Paste | |
| `⌘⇧V` | Paste Attributes | Copy màu / transform / speed |
| `⌘D` | Add transition mặc định | Cross dissolve nhanh |
| `⌘⇧[` / `]` | Snapping on/off (hoặc `N`) | Bật/tắt hút cạnh |
| `N` | Toggle Snapping | Rất hay dùng |
| `⌘+` / `⌘-` | Zoom timeline | |
| `⇧Z` | Fit timeline to window | Nhìn toàn bộ |
| `⌥Y` | Select clips forward trên track active | Dời cả chuỗi phía sau |
| `Y` | Select clip tại playhead | |
| `⌘A` | Select all | |
| `S` | Toggle Mute track? *(kiểm tra keymap)* / thường dùng Soft clip controls | Xem Keyboard Customization |
| `⌘S` | Save | Thói quen mỗi vài phút |

> Một số phím có thể khác theo phiên bản/keymap. Nếu không khớp: mở **Keyboard Customization** → search tên lệnh.

---

## 2. Cắt dựng & chỉnh clip

| Phím | Chức năng |
|------|-----------|
| `⌘⇧,` / `⌘⇧.` | Trim clip start / end về playhead (ripple trim) |
| `[` / `]` | Trim start / end về playhead (không ripple — tùy keymap) |
| `,` / `.` | Nudge clip 1 frame trái/phải |
| `⇧,` / `⇧.` | Nudge lớn hơn |
| `⌘⌫` | Delete + close gap (ripple) trên selection |
| `P` | Pen tool (keyframe trên inspector/curve) |
| `C` | Cut/Blade tool (một số keymap) |
| `T` | Trim tool |
| `⌘R` | Rename |
| `⌘L` | Linked selection on/off (video+audio) |
| `⌥[click]` | Unlink tạm khi kéo |

---

## 3. Timeline / Track / Navigation

| Phím | Chức năng |
|------|-----------|
| `⌘↑` / `⌘↓` | Chọn track trên / dưới |
| `⌥⌘W` | Close gap (nếu có trong keymap) |
| `PageUp` / `PageDown` | Nhảy clip trước / sau |
| `↑` / `↓` | Previous / Next edit point |
| `⇧⌘Left/Right` | Select to start/end |
| `M` | Marker |
| `⇧M` | Marker & modify |
| `⌘M` | Delete marker (kiểm tra keymap) |
| `Ctrl-` / `Ctrl=` *(Win)* | Zoom — Mac dùng `⌘±` |

---

## 4. Playback & Viewer

| Phím | Chức năng |
|------|-----------|
| `⌘/` | Full screen viewer |
| `⇧Z` | Zoom fit |
| `⌥⌘F` | Source/Timeline viewer toggle (kiểm tra) |
| `Ctrl-P` / Pause related | Pause |
| `/` (numpad) | Enter edit mode variants |

Loop đoạn In–Out: bật **Loop** trên transport, set `I`/`O`.

---

## 5. Color page (nhanh)

| Phím | Chức năng |
|------|-----------|
| `⌘D` | (Edit) transition — trên Color: thêm serial node thường là `⌥S` |
| `⌥S` | Add Serial Node |
| `⌥P` | Add Parallel Node |
| `⌥L` | Add Layer Node |
| `⌫` | Delete node |
| `⌘Z` | Undo grade |
| `⌘C` / `⌘V` | Copy / Paste grade |
| `⌘⇧V` | Paste grade to selected |
| `⌘/` | Full screen |

Preset: tạo **PowerGrade** library để apply 1 click (quan trọng hơn nhớ hết phím Color).

---

## 6. Fairlight (audio)

| Phím | Chức năng |
|------|-----------|
| `A` | Selection |
| `B` | Blade audio |
| `⇧⌫` | Ripple delete khoảng lặng |
| `⌘⇧C` | *(nếu map)* Bounce/mix related — kiểm tra keymap |
| Fade | Kéo fade handle góc clip hoặc keyframe volume |

Khuyến nghị: map thêm **Add transition (audio crossfade)** vào phím dễ bấm.

---

## 7. Deliver / Export

| Phím / hành động | Mục đích |
|------------------|----------|
| `⌘⇧D` hoặc click Deliver | Vào trang xuất *(tuỳ keymap)* |
| Lưu **Preset** YouTube 1080p / Shorts 1080×1920 | 1 click export |
| `Render All` | Queue |

---

## 8. Custom keymap nên tạo (rất đáng)

Vào **Keyboard Customization** → đặt phím dễ nhớ cho:

| Lệnh nên map | Gợi ý phím |
|--------------|------------|
| Ripple Delete | `⇧⌫` (nếu chưa có) |
| Blade All Tracks | `⌘B` |
| Paste Attributes | `⌘⇧V` |
| Toggle Snapping | `N` |
| Select Clips Forward on This Track | `⌥Y` |
| Add Video Transition | `⌘D` |
| Add Audio Crossfade | `⌘⇧D` (nếu Deliver không đụng) |
| Retime Controls | `⌘R` (hoặc phím khác nếu trùng Rename) |
| Stabilization enable | tự map |
| New Timeline | tự map |

Export keymap: **Keyboard Customization → Export** để backup / dùng máy khác.

---

## 9. Workflow “edit viral” chỉ bằng phím

1. Import → kéo clip vào timeline  
2. `J/K/L` duyệt → `B` cắt dead air → `⇧⌫` ripple  
3. `I`/`O` chọn đoạn hay → copy sang timeline Shorts  
4. `⌘D` transition nhẹ (không lạm dụng)  
5. Caption: dùng Text+ (Fusion Text+) hoặc subtitle track  
6. Color: `⌥S` node + PowerGrade  
7. Audio: blade khoảng ồn, fade nhạc  
8. Deliver preset YouTube / Vertical  

---

## 10. Cheat-sheet 1 trang (in / dán cạnh màn hình)

```
PLAY:  Space  J K L  ← →
CUT:   B  ⌘B  ⇧⌫  ⌘D
MARK:  I O  ⌥X
MOVE:  , .  ⌥Y  N (snap)
EDIT:  F9 Insert  F10 Overwrite  F12 On Top
COLOR: ⌥S node  ⌘C/V grade
SAVE:  ⌘S
```

---

## Tài liệu chính thức

- Blackmagic: *DaVinci Resolve Manual* → Keyboard Shortcuts  
- In-app: **Workspace → Keyboard Customization**
