# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session11_EXontap
## Phần 1 – Hoàn thiện SRS & Auto TOC

1. **Khung tiêu đề 3 cấp:**
* 1. Giới thiệu dự án (H1)


* 1.1. Mục tiêu (H2) | 1.2. Đối tượng sử dụng (H2)


* 2. Chức năng hệ thống (H1)


* 2.1. Quản lý mượn sách (H2)
* 2.1.1. Luồng mượn sách qua thẻ sinh viên (H3)


* 2.2. Quản lý trả sách (H2)


* 3. Yêu cầu bảo mật (H1)




2. **Nội dung mô tả:**
* Mục 2 (Functional): Ghi nhận giao dịch mượn/trả và cảnh báo quá hạn.
* Mục 3 (Non-functional): Mã hóa dữ liệu lưu trữ và phân quyền Admin.


3. **Auto TOC:** *References* -> *Table of Contents* -> Chọn mẫu. Cập nhật: Chuột phải vào mục lục -> *Update Field* -> *Update entire table*.

---

## Phần 2 – Chuẩn hóa dữ liệu & AutoFilter

1. **3 lỗi vi phạm:**
* Lỗi 1: Trộn ô Hàng 1 (A1:E1) -> Vi phạm quy tắc không merge ô.
* Lỗi 2: Hàng trống ở Hàng 5 -> Vi phạm quy tắc không có hàng trống trong vùng dữ liệu.
* Lỗi 3: Dòng tổng cộng ở Hàng 6 -> Vi phạm quy tắc không chứa dòng tổng kết bên trong bảng.


2. **Phân biệt Record & Field:**
* Record: 1 dòng thông tin của một sinh viên mượn sách.
* Field: 1 cột thuộc tính (`MSSV` hoặc `Tình Trạng`).


3. **Thao tác AutoFilter:** Chọn bảng -> Nhấn `Ctrl + Shift + L` -> Lọc cột *Tình Trạng* chọn *Quá hạn*.

---

## Phần 3 – VLOOKUP

1. **Công thức VLOOKUP tại F2:**
`=VLOOKUP(C2, DanhMucSach!$A$2:$C$4, 2, FALSE)`
2. **Lỗi mã `S099`:** Trả về `#N/A` do mã sách không tồn tại trong bảng tra cứu.
3. **Công thức bọc IFERROR:**
`=IFERROR(VLOOKUP(C2, DanhMucSach!$A$2:$C$4, 2, FALSE), "Không tìm thấy sách")`

---

## Phần 4 – Slide báo cáo tiến độ

1. **Nội dung Slide:**
* **Assertion Title:** *Tháng 10 ghi nhận 4 lượt mượn: 25% quá hạn và 25% lỗi dữ liệu mã sách.*
* **Nội dung chính:** Tỷ lệ quá hạn và lỗi nhập liệu cần xử lý.
* **Biểu đồ:** **Donut Chart** (phù hợp để thể hiện tỷ trọng các trạng thái mượn sách).


2. **Rule 10/20/30:** 1 slide trong tổng 10 slide; thời gian trình bày 2 phút.
