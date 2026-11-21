# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): nguyenduccuong        Người kiểm (học viên): phammanhhung  
Ngày: 21/11/2026                          Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): nguyenduccuong-front.zip, nguyenduccuong-fisheye.zip (revision 1)  
Số ảnh kiểm: 6 (+ 0 ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag): 81  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 6 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 12 | 0 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 17 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 17 | 1 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 17 | 1 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 17 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 10 | 1 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 9 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 19 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 10 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 7 | 0 | chính |
| QC1-12 file | lỗi file | 2 | 0 | nhẹ / nặng |

*Ghi chú về quy tắc của lớp:* Theo hướng dẫn trực tiếp của giảng viên, các vạch đôi được vẽ/chấm cả 2 nét polyline riêng nên các vạch mang cùng position ở vạch đôi (như tại A04) không tính là lỗi tách vạch QC1-05. Các ảnh không có vạch sơn thực tế (như A07) không vẽ vạch ảo và được miễn trừ lỗi QC1-02.

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-04 | A01 | lane (L2, y: 505 -> 600) | chính | Điểm đầu cao hơn điểm cuối (y=505 ở xa, y=600 ở gần): polyline vẽ ngược chiều từ xa về gần. |
| 2 | QC1-05 | A08 | lane (L1) | chính | Vạch L1 đơn bị ngắt quãng thành 2 polyline riêng (đoạn liền và đoạn đứt nối tiếp) thay vì 1 đường duy nhất. |
| 3 | QC1-07 | B06 | drivable | chính | Bỏ sót không gán polygon drivable cho vùng mặt đường xe chạy được trên ảnh camera hông B06. |

*Ảnh không lỗi đối chiếu:* Ảnh **B01** (`B01_02688_FV.png`) đạt chuẩn: đủ 4 tag đúng, crosswalk (26 điểm), 2 road_curb (mỗi đường 12 điểm uốn cong fisheye chuẩn xác), polygon drivable ôm sát, đèn tín hiệu red ôm sát vỏ hướng front, không có bất kỳ lỗi nào.

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A07 | Ảnh A07 phía bên trái sát dải phân cách/lề không có vạch sơn rõ ràng nên không gán vạch L1, có được miễn QC1-02 không? | Xác nhận miễn lỗi nếu thực tế ảnh không thấy vạch theo hướng dẫn Checkpoints. |

## Quyết định
Lỗi nặng: 0   Lỗi chính: 3 / 81 nhãn = 3.70 %   Lỗi nhẹ: 1 (A04 có 1 box biển phụ <8px)   Ca chờ lead: 1  
Quyết định (Release / Hold / Rework): **Release**  
Lý do (theo luật của phiếu): Không có lỗi nặng. Tỉ lệ lỗi chính là 3.70 % (dưới ngưỡng quy định 5 % số nhãn đã kiểm). Quy tắc vạch đôi chấm cả 2 nét theo hướng dẫn của giảng viên đã được áp dụng. Đạt yêu cầu bàn giao lô.
