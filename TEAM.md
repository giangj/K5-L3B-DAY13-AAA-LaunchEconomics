# Team

## Thông tin nhóm

- Tên nhóm: AAA
- Lớp: L3B
- Repo nhóm: `K5-L3B-DAY13-AAA-LaunchEconomics` (xem [SUBMISSION.md](SUBMISSION.md))
- URL repo, nhánh nộp, commit chốt: `https://github.com/giangj/K5-L3B-DAY13-AAA-LaunchEconomics`, nhánh `main` (PR duyệt chéo từ nhánh `LeGiang-p4-03912`)

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Lê Thế Anh | 2A202603983 | f412626284@outlook.com | LETHESHIYING | P1 — Người viết code (lượt 1) |
|   2 | Nguyễn Xuân Đạt | 2A202603958 | xuandat31804@gmail.com | chipno39 | P2 — Người kiểm số / Người viết code (lượt 2) |
|   3 | Trần Xuân Lộc | 2A202603951 | xuanloca2tv@gmail.com | Kaylez-TXL | P3 — Người gắn nhãn 1 |
|   4 | Lê Danh Giang | 2A202603912 | anhgiang210@gmail.com | giangj | P4 — Người gắn nhãn 2 kiêm giữ hồ sơ |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

Đổi người viết code sau giờ giải lao, để ít nhất hai người trong nhóm tự tay tính được chi phí.

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/team/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

## Lê Thế Anh-2A202603983

### Phần việc phụ trách

- P1 — Người viết code (lượt 1): triển khai phần A1–A4, B1–B4 trong `src/lab13.py`, phân chia nhiệm vụ nhóm.

### Đóng góp cụ thể

- Viết 3 hàm A1 (`so_lan_chay_ky_vong`, `ti_le_thanh_cong`, `he_so_chi_phi_moi_viec_thanh_cong`) qua đủ 3 phép thử đáp án biết trước (`1,20 · 1,25 · 1,25`).
- Viết hàm `mo_hinh()` và kịch bản tách loại A3, chi phí cố định A4, độ nhạy B1–B4 trong `src/lab13.py`.

### Bằng chứng

- Commit `5af9559`, `9ab8462` (PR #4 `ec0ebd9`) trên nhánh `main`, [src/lab13.py](src/lab13.py), [PHAN_CONG.md](PHAN_CONG.md) và [report/team/2A202603983_LeTheAnh.md](report/team/2A202603983_LeTheAnh.md).

## Nguyễn Xuân Đạt-2A202603958

### Phần việc phụ trách

- P2 — Người kiểm số và Người viết code (lượt 2): kiểm tay đối chiếu số A–B, điền `report/team/bang_chi_phi.md`, bổ sung phần tính cỡ mẫu D1 trong `src/lab13.py`.

### Đóng góp cụ thể

- Kiểm tay đối chiếu số lượng `thanh_cong`, chi phí tool/xem lại/làm lại từ CSV và điền đầy đủ bảng A1–A4, B1–B4 trong `report/team/bang_chi_phi.md`.
- Viết phần tính cỡ mẫu D1 (5 câu a–e, power khi MDE 6 điểm, tỉ lệ `mo_lai_trong_7_ngay`) ở cuối `src/lab13.py` và bàn giao số liệu cho P3, P4.

### Bằng chứng

- Commit `ebc27b4` (PR #1 `f43294c`) và `55eb303` trên nhánh `main`, [src/lab13.py](src/lab13.py), [report/team/bang_chi_phi.md](report/team/bang_chi_phi.md) và [report/team/2A202603958_NguyenXuanDat.md](report/team/2A202603958_NguyenXuanDat.md).

## Trần Xuân Lộc-2A202603951

### Phần việc phụ trách

- P3 — Người gắn nhãn 1: gắn nhãn độc lập 20 ca lỗi, lập bảng khắc phục 5 ca, thiết kế `report/team/pilot_plan.yaml` và danh sách event trong `report/team/chi_so.md`.

### Đóng góp cụ thể

- Hoàn thành cột Nhãn người 1 (20 ca), quy tắc phân biệt và bảng khắc phục 5 ca đại diện đủ 5 loại Google PAIR trong `report/team/bang_loi.md`.
- Hoàn thiện `report/team/pilot_plan.yaml` (D1, D2, đánh đổi MDE +6 điểm, 3 luật dừng đủ 4 vế `NẾU–TRONG–THÌ–KHÔNG THÌ`, rollback) và 10 event có `trace_id` kèm kiểm tra chéo trong `report/team/chi_so.md`.

### Bằng chứng

- Các commit `69c3f3b`, `aa30f3e`, `8b52b3b` (PR #2 `8bc87ae`), `a86f753`, `c900aa1` trên nhánh `main`, [report/team/pilot_plan.yaml](report/team/pilot_plan.yaml), [report/team/chi_so.md](report/team/chi_so.md), [report/team/bang_loi.md](report/team/bang_loi.md) và [report/team/2A202603951_TranXuanLoc.md](report/team/2A202603951_TranXuanLoc.md).

## Lê Danh Giang-2A202603912

### Phần việc phụ trách

- P4 — Người gắn nhãn 2 kiêm giữ hồ sơ: gắn nhãn độc lập 20 ca lỗi và chốt đồng thuận, hoàn thiện E1/E2 trong `report/team/chi_so.md`, tổng hợp `report/team/ho_so_launch_v0.md`, `report/team/group_report.md`, `TEAM.md` và kiểm tra checklist nộp bài.

### Đóng góp cụ thể

- Gắn nhãn độc lập 20 ca lỗi (cột Nhãn người 2), đối chiếu với P3 đạt đồng thuận `20/20` (`100%`) trong `report/team/bang_loi.md`.
- Tính thử 3 chỉ số E1 từ `src/logix_requests.csv`, hoàn thiện 2 chỉ số tự đề xuất và 3 dòng rủi ro kinh tế E2 trong `report/team/chi_so.md`.
- Tổng hợp 7 mục + đề xuất `Go có điều kiện` trong `report/team/ho_so_launch_v0.md`, viết `report/team/group_report.md`, điền `TEAM.md` và báo cáo cá nhân `report/team/2A202603912_LeDanhGiang.md`.

### Bằng chứng

- Nhánh `LeGiang-p4-03912`, PR vào `main`, các file [TEAM.md](TEAM.md), [report/team/bang_loi.md](report/team/bang_loi.md), [report/team/chi_so.md](report/team/chi_so.md), [report/team/ho_so_launch_v0.md](report/team/ho_so_launch_v0.md), [report/team/phieu_cham.md](report/team/phieu_cham.md), [report/team/group_report.md](report/team/group_report.md), [report/team/2A202603912_LeDanhGiang.md](report/team/2A202603912_LeDanhGiang.md).
