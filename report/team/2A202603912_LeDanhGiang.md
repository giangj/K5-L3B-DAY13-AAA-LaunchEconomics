# Báo cáo cá nhân — Lê Danh Giang - 2A202603912

## 1. Thông tin thành viên

- Họ tên: Lê Danh Giang
- MSSV: 2A202603912
- Email: anhgiang210@gmail.com
- Vai trong nhóm (người viết code, người kiểm số, người gắn nhãn 1, người gắn nhãn 2 kiêm giữ hồ sơ): Người gắn nhãn 2 kiêm giữ hồ sơ (P4)

## 2. Phần việc phụ trách

- Gắn nhãn độc lập 20 ca lỗi theo 5 loại của Google PAIR (Nhiệm vụ C, cột Nhãn người 2), so khớp với P3 và chốt tỉ lệ đồng thuận trong [bang_loi.md](bang_loi.md).
- Hoàn thiện phần tính chỉ số E1 trên 1.200 yêu cầu, 2 chỉ số tự đề xuất và bảng 3 rủi ro kinh tế E2 trong [chi_so.md](chi_so.md).
- Tổng hợp bộ hồ sơ 1 trang (7 mục + đề xuất `Go có điều kiện`) trong [ho_so_launch_v0.md](ho_so_launch_v0.md).
- Hoàn thiện [TEAM.md](../../TEAM.md), [group_report.md](group_report.md), tham gia duyệt chéo Gate 2a cho Nhóm 4 trong [phieu_cham.md](phieu_cham.md) và kiểm tra toàn bộ checklist nộp bài trước khi mở PR vào nhánh `main`.

## 3. Đóng góp cụ thể

- Đọc và phân loại độc lập 20 ca lỗi từ `docs/Ngay13_Lab13_De_bai_hoc_vien.docx` dựa trên nguyên nhân gốc (4 Do người dùng, 5 Hệ thống, 4 Ngữ cảnh, 4 Giới hạn hệ thống, 3 Ngầm), đối chiếu với P3 đạt đồng thuận `20/20` (`100%`).
- Tính trực tiếp từ `src/logix_requests.csv` ba chỉ số E1 cho đợt chạy thử: chỉ số chính `82,83%` (`994/1.200`), tỉ lệ bỏ qua gợi ý `27,12%` (`48/177`), tỉ lệ mở lại 7 ngày `4,25%` (`51/1.200`; trong phạm vi `noi_dia + hang_nang` là `3,97%`, `39/982`, và tỉ lệ làm lại là `4,89%`, `48/982`).
- Hoàn thiện bảng rủi ro kinh tế E2 từ kết quả độ nhạy của P2 (làm lại ×2 tăng `+51,8%`, xem lại 100% lên `0,98×–1,03×`, giảm nửa khối lượng tăng chi phí cố định lên `2.370 đ/việc`).
- Tổng hợp 7 mục hồ sơ trong `ho_so_launch_v0.md` kèm đề xuất **Go có điều kiện** với 4 điều kiện cụ thể, có vai trò phụ trách và ngày kiểm tra rõ ràng; đảm bảo toàn bộ số giả lập đều có nhãn `simulated`, không dùng từ cấm và không ghi người phụ trách là "cả đội".
- Đọc và thẩm định 5 file hồ sơ của Nhóm 4 (`K5-L3B-DAY13-Nhom4-LaunchEconomics`), điền phiếu chấm `30/30` với quyết định `Go có điều kiện` kèm câu hỏi kiểm tra tại [phieu_cham.md](phieu_cham.md), đồng thời cập nhật kết quả duyệt chéo `30/30` của nhóm AAA vào [group_report.md](group_report.md).

## 4. Bằng chứng

- Nhánh làm việc `LeGiang-p4-03912` và các PR gộp vào `main` trên repo `K5-L3B-DAY13-AAA-LaunchEconomics`.
- Các file đã cập nhật và tạo mới:
  - [TEAM.md](../../TEAM.md)
  - [report/team/bang_loi.md](bang_loi.md)
  - [report/team/chi_so.md](chi_so.md)
  - [report/team/ho_so_launch_v0.md](ho_so_launch_v0.md)
  - [report/team/phieu_cham.md](phieu_cham.md)
  - [report/team/group_report.md](group_report.md)
  - [report/team/2A202603912_LeDanhGiang.md](2A202603912_LeDanhGiang.md)

## 5. Công cụ AI đã dùng

- Sử dụng trợ lý AI trong IDE để trích xuất văn bản 20 ca lỗi từ file `.docx`, hỗ trợ tổng hợp văn bản hồ sơ và rà soát checklist định dạng.
- Tự kiểm tra kết quả bằng cách chạy script Python kiểm chứng trực tiếp các con số E1 trên `src/logix_requests.csv`, chạy `src/lab13.py` kiểm tra toàn bộ A–D1, kiểm tra `pilot_plan.yaml` bằng `yaml.safe_load`, và quét lại toàn bộ thư mục `report/team/` để đảm bảo không sót dấu `?`, không thiếu nhãn `simulated` và không vi phạm quy tắc đặt tên/từ ngữ.

## 6. Tự đánh giá

- Hoàn thành đầy đủ phần việc của P4 đúng vai trò và đồng bộ số liệu với các thành viên P1, P2, P3.
- Hoàn thành đầy đủ toàn bộ phần việc của P4 và tài liệu duyệt chéo Gate 2a ([phieu_cham.md](phieu_cham.md), [group_report.md](group_report.md)), đồng bộ 100% số liệu với P1, P2, P3 và đạt toàn bộ checklist nộp bài trong `SUBMISSION.md`.
