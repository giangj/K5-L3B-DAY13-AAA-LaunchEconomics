# Báo cáo nhóm

Báo cáo ngắn, tối đa 2 trang. Số liệu chi tiết nằm trong các file hồ sơ; ở đây chỉ dẫn lại con số chính.

## 1. Thông tin nhóm

- Tên nhóm: AAA
- Lớp: L3B
- Thành viên: xem [TEAM.md](../../TEAM.md)

## 2. Mục tiêu và cách tiếp cận

Xây dựng bộ **hồ sơ launch v0** trình hội đồng **Gate 2a** để duyệt kế hoạch **pilot** (không phải duyệt chạy chính thức) cho trợ lý hoàn phí của LogiX-VN, dựa trên mẫu giả lập 1.200 yêu cầu (1.624 lần chạy) từ đợt chạy thử 2 tuần ở 6 depot. Cách tiếp cận bám sát 4 câu hỏi cốt lõi: tính chi phí thật cho mỗi việc thành công, phân loại lỗi theo nguyên nhân gốc (Google PAIR), thiết kế pilot có đối chứng và đủ cỡ mẫu (xét hiệu ứng cụm ICC), và đặc tả hệ thống chỉ số/event theo dõi rủi ro kinh tế.

## 3. Giải pháp

- **Nhiệm vụ A & B (Mô hình chi phí & độ nhạy):** Cài đặt 3 hàm A1 (qua test `1,20 · 1,25 · 1,25`), hàm `mo_hinh()` tính token, tool (mọi lần chạy kể cả lỗi) và giờ nhân viên xem lại/làm lại (`_simulated`), tách theo 4 loại yêu cầu, cộng chi phí cố định 40 triệu đ/tháng và chạy 9 kịch bản độ nhạy + giới hạn 1–3 lần chạy trong [src/lab13.py](../../src/lab13.py) và [bang_chi_phi.md](bang_chi_phi.md).
- **Nhiệm vụ C (Bảng lỗi & khắc phục):** Hai thành viên P3 và P4 gắn nhãn độc lập 20 ca lỗi theo 5 loại Google PAIR, đối chiếu đạt đồng thuận `20/20` (`100%`) và lập bảng phát hiện đo được + khắc phục cho 5 ca đại diện trong [bang_loi.md](bang_loi.md).
- **Nhiệm vụ D (Kế hoạch pilot):** Tính cỡ mẫu 5 câu D1 trong [src/lab13.py](../../src/lab13.py), kiểm tra 5 câu tách tác động D2, chọn phương án chia theo nhân viên (`20 + 20`), ghi rõ đánh đổi MDE `+6 điểm` và 3 luật dừng đủ 4 vế `NẾU–TRONG–THÌ–KHÔNG THÌ` trong [pilot_plan.yaml](pilot_plan.yaml).
- **Nhiệm vụ E (Chỉ số, event, rủi ro & hồ sơ):** Tính 3 chỉ số trên 1.200 yêu cầu, đề xuất thêm 2 chỉ số, thiết kế 10 event gắn `trace_id`, tổng hợp 3 rủi ro kinh tế trong [chi_so.md](chi_so.md) và đóng gói thành hồ sơ 1 trang trong [ho_so_launch_v0.md](ho_so_launch_v0.md).

## 4. Kết quả

- **Chi phí thật & phạm vi:** Toàn mẫu đạt `4.472 đ/việc thành công` (`simulated`), gấp `16,3×` hoá đơn token+tool/yêu cầu (`274,7 đ`); giờ nhân viên chiếm `92,5%`. Khi cộng 222 ca không thành công do nhân viên làm thay, chi phí cả hệ thống là `5.865 đ/yêu cầu = 0,49×` của `12.000 đ` (`simulated`). Chỉ `noi_dia` (`0,22×`, `2.696 đ`, `simulated`) và `hang_nang` (`0,69×`, `8.221 đ`, `simulated`) hiệu quả rõ rệt; `quoc_te` (`1,88×`, thành công `27,3%`) và `doi_tac` (`0,85×`, điều khoản riêng) được loại khỏi pilot. Cộng chi phí cố định 40 triệu/tháng cho phạm vi `noi_dia + hang_nang` cho `4.599 đ` (`0,38×`, `simulated`) ở 45.000 yc/tháng và `5.784 đ` (`0,48×`, `simulated`) ở nửa khối lượng.
- **Độ nhạy & giới hạn chạy lại:** Ba yếu tố nhạy nhất là số ca làm lại (`+51,8%` khi ×2), tỉ lệ xem lại (`+40,7%` khi ×2) và lương nhân viên (`+23,1%` khi +25%) (`simulated`). Giới hạn 2 lần chạy rẻ nhất cả hệ thống (`6.901.220 đ`, `simulated`). Xem lại 100% đẩy chi phí lên `11.743 đ = 0,98×` (9 phút làm lại) hoặc `12.415 đ = 1,03×` (15,3 phút làm lại) (`simulated`).
- **Chỉ số đợt chạy thử & lỗi:** Chỉ số chính trong đợt chạy thử là `82,83%` (`994/1.200`), bỏ qua gợi ý `27,12%` (`48/177`), mở lại 7 ngày `4,25%` (`3,97%` trong `noi_dia + hang_nang`). Gắn nhãn lỗi đạt đồng thuận `20/20` (`100%`).
- **Đề xuất cuối tại [ho_so_launch_v0.md](ho_so_launch_v0.md):** **Go có điều kiện** cho kế hoạch pilot phạm vi `noi_dia + hang_nang`, kèm 4 điều kiện có người phụ trách và hạn kiểm tra.
- **Kết quả duyệt chéo Gate 2a:** Nhóm AAA đạt **30/30 điểm** từ hội đồng duyệt chéo cho hồ sơ launch v0 (đề xuất **Go có điều kiện**). Ở vai trò hội đồng, nhóm AAA đã chấm hồ sơ Nhóm 4 (`K5-L3B-DAY13-Nhom4-LaunchEconomics`) đạt **30/30 điểm** với quyết định **Go có điều kiện** và ghi nhận đầy đủ tại [phieu_cham.md](phieu_cham.md).

## 5. Khó khăn và cách xử lý

- **Không đủ cụm cho MDE +5 điểm:** Với 40 nhân viên (`20 + 20`) và `ICC = 0,02`, cỡ mẫu hiệu dụng tối đa là `1.000 < 1.251`. Nhóm chọn chia theo nhân viên và nâng MDE lên `+6 điểm` (`n = 859/nhóm`, `m ≥ 299` yc/người), đồng thời công khai rủi ro power giảm còn `0,64` nếu tác động thật chỉ đạt `+5 điểm`.
- **Phụ thuộc số liệu `_simulated`:** Thời gian xem lại/làm lại hiện là giả lập nên nhóm gắn nhãn `simulated` ở mọi con số liên quan và đưa điều kiện thu thập thời gian thật qua event ngay tuần 1 pilot.
- **Đặt ngưỡng dừng an toàn:** Tỉ lệ mở lại hiện tại là `4,25%` (`3,97%` trong phạm vi), nên nhóm không đặt ngưỡng tuyệt đối thấp hơn mức hiện tại mà dùng ngưỡng chênh `+2 điểm` so với đối chứng kèm trần `6%`.

## 6. Tổng hợp đóng góp

Chi tiết phân vai (P1–P4), đóng góp và bằng chứng commit của từng thành viên nằm trong [TEAM.md](../../TEAM.md).

## 7. Hạn chế và hướng cải thiện

- Đợt chạy thử 2 tuần chưa có nhóm đối chứng nên chưa thể kết luận tác động nhân quả (không kết luận trợ lý nâng chỉ số).
- Dữ liệu thời gian nhân viên là giả lập; cần triển khai đủ 10 event có `trace_id` để đo thời gian xem lại/làm lại thực tế và xác định ngưỡng giảm tỉ lệ xem lại an toàn.
- Nếu cần phát hiện chắc chắn mức chênh `+5 điểm` với power `0,80`, cần kéo dài thời gian pilot hoặc mở rộng đội ngũ CSKH vượt mức 40 nhân viên hiện tại.

## 8. Tài liệu tham khảo

- Erol et al., *Cost-of-Pass: An Economic Framework for Evaluating Language Models*, [arxiv.org/abs/2504.13359](https://arxiv.org/abs/2504.13359)
- Google PAIR, *People + AI Guidebook*, chương "Errors + Graceful Failure", [pair.withgoogle.com](https://pair.withgoogle.com)
- Tài liệu `statsmodels`, lớp `NormalIndPower` (`stats.power`)
