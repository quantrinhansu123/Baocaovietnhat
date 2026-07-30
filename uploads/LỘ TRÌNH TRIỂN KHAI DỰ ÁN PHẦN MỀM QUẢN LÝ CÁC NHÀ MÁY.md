# **LỘ TRÌNH TRIỂN KHAI CỦA PHÒNG IT**

# **PHẦN MỀM QUẢN LÝ SẢN XUẤT NHÀ MÁY TẠI TẬP ĐOÀN VIỆT NHẬT**

## **Timeline triển khai từ tháng 07/2026 đến sau Go-Live 01/01/2027**

Mục tiêu của kế hoạch là đảm bảo phần mềm được triển khai theo từng giai đoạn rõ ràng, có thời gian kiểm thử, chạy song song, đối soát số liệu thực tế giữa phần mềm và quy trình hiện hành, đào tạo người sử dụng và hoàn thiện hệ thống trước khi đưa vào vận hành chính thức trên toàn bộ các nhà máy của Tập đoàn Việt Nhật; đồng thời đáp ứng luồng nghiệp vụ thực tế của các Nhà máy như Nhà máy Đà Nẵng và Nhà máy Phú Thọ, cụ thể:

![][image1]

# **I. LỘ TRÌNH TỔNG THỂ**

# **1\. Timeline tổng thể**

| Giai đoạn | Thời gian | Mục tiêu chính | Đầu ra |
| :---: | :---: | ----- | :---: |
| Giai đoạn 1 | 07/2026 | Phân tích nghiệp vụ, thiết kế, lập trình và kiểm thử nội bộ | Phiên bản Beta 1.0 |
| Giai đoạn 2 | 08–09/2026 | Triển khai tại Nhà máy Đà Nẵng và Nhà máy Phú Thọ, chạy song song, đối soát số liệu và hoàn thiện hệ thống | Phiên bản gần chính thức (RC) |
| Giai đoạn 3 | 10–12/2026 | Triển khai chính thức tại toàn bộ các nhà máy và đơn vị thuộc Tập đoàn | Phần mềm Quản lý Nhà máy |
| Giai đoạn 4 | Từ 01/01/2027 | Vận hành, bảo trì và nâng cấp định kỳ | Các phiên bản nâng cấp |

# **2\. Biểu đồ Timeline tổng hợp**

![][image2]

# **3\. Kết quả đầu ra của từng giai đoạn**

* Tháng 07/2026: Hoàn thành khảo sát, phân tích nghiệp vụ, thiết kế hệ thống, phát triển các phân hệ cốt lõi (Kế hoạch sản xuất, Lệnh sản xuất, BOM, Kho nguyên vật liệu, Kho thành phẩm, QC, Dashboard) và phát hành phiên bản phần mềm Beta.

* Tháng 08–09/2026: Triển khai chạy thực tại Nhà máy Đà Nẵng và Nhà máy Phú Thọ, vận hành song song với quy trình hiện tại, đối soát dữ liệu về kế hoạch sản xuất, định mức BOM, tiêu hao nguyên vật liệu, tồn kho, chất lượng và sản lượng; hoàn thiện hệ thống, phát hành bản gần chính thức Release Candidate (RC).

* Tháng 10–12/2026: Triển khai Go-Live theo từng đợt tại toàn bộ các nhà máy và đơn vị thuộc Tập đoàn Việt Nhật, hoàn tất nghiệm thu, bàn giao video hướng dẫn từng nhóm đối tượng, tài liệu hướng dẫn và đưa vào vận hành Phần mềm Quản lý Nhà máy Sản xuất Version 1.0.

* Từ 01/01/2027: Hệ thống vận hành ổn định, thực hiện bảo trì và nâng cấp định kỳ theo chu kỳ 3 tháng/lần, bổ sung các chức năng mới, tối ưu hiệu năng, mở rộng tích hợp với các hệ thống ERP, Kế toán, IoT và thiết bị sản xuất khi có nhu cầu, phát triển thành các phiên bản Version 2.0; Version 3.0.

# **II. LỘ TRÌNH CHI TIẾT**

# **1\. Giai đoạn 1 – Phân tích, thiết kế và phát triển (Tháng 07/2026)**

## **Tuần 1–2 (01/07 – 14/07)**

### **Phân tích nghiệp vụ**

* Khảo sát quy trình sản xuất tại các nhà máy:

  * Luồng nghiệp vụ Đơn đặt hàng sản xuất

  * Nghiệp vụ Quản đốc sản xuất, Công nhân

  * Khảo sát nghiệp vụ Thống kê & QC

  * Khảo sát Kho nguyên vật liệu

  * Khảo sát Kho thành phẩm

* Chuẩn hóa dữ liệu từ Excel, Google Sheet

* Thống nhất luồng nghiệp vụ tổng thể với Ban Lãnh đạo

* Hoàn thiện, chốt các yêu cầu về phần mềm, tài liệu lập trình

### **Thiết kế hệ thống**

* Thiết kế Database

* Thiết kế API

* Thiết kế UI/UX

* Thiết kế phân quyền

* Thiết kế báo cáo quản trị

### **Lập trình Backend**

* Xác thực, đăng nhập

* Danh mục

* BOM

* Kế hoạch sản xuất/LSX

* Kho nguyên vật liệu

* Xuất vật tư

* Nhật ký sản xuất

* Nhật ký phối trộn & QC

* Thành phẩm

* Dashboard

### **Lập trình Frontend**

* Các biểu mẫu/các báo cáo

* Kế hoạch sản xuất

* Lệnh sản xuất

* BOM

* Kho

* Sản xuất

* Nhật ký phối trộn & QC

### **Cài đặt hệ thống**

* PostgreSQL / Supabase

* Application Server

* Domain

### **Sản phẩm bàn giao**

* Phiên bản Beta:  [https://chuyendoicongtyvietnhatipt.vercel.app/](https://chuyendoicongtyvietnhatipt.vercel.app/) đã được bàn giao cho Nhà máy Đà Nẵng để chạy thử

## **Tuần 3–4 (15/07 – 31/07)**

### **Kiểm thử nội bộ**

Kiểm thử toàn bộ các phân hệ: Kế hoạch sản xuất/LSX, Xuất NVL, Nhật ký sản xuất, Giao ca, BOM, Nhật ký phối trộn & QC, Thành phẩm, Báo cáo

Đồng thời:

* Test API

* Test phân quyền

* Test công thức BOM

* Test định mức hao hụt

* Test hiệu năng

* Test bảo mật

### **Kết quả**

Hoàn thiện phiên bản Beta để triển khai Pilot.

# **2\. Giai đoạn 2 – Pilot tại Nhà máy Đà Nẵng và Nhà máy Phú Thọ (Tháng 08–09/2026)**

## ***a. Tháng 08/2026***

### **Tuần 1–2 (01/08 – 14/08)**

### **Cài đặt hệ thống**

* Database riêng từng nhà máy

* Server

* Domain

* Backup

* Phân quyền

### **Import dữ liệu nền tảng (MASTER DATA) của từng Nhà máy**

* Danh mục sản phẩm

* Danh mục nguyên vật liệu

* BOM

* Danh mục Máy

* Các Kho NVL, Kho thành phẩm

* Nhà cung cấp

* Khách hàng

* Nhân viên, chức danh

### **Hướng dẫn, hỗ trợ các bộ phận**

Hướng dẫn các bộ phận thao tác, bắt đầu sử dụng, thực hiện song song trên phần mềm mới và phương pháp cũ cho các bộ phận:

* Kinh doanh

* Kế hoạch sản xuất

* Quản đốc

* Công nhân

* Thống kê & QC

* Kho nguyên vật liệu, Kho thành phẩm

### **Bắt đầu chạy song song**

Các bộ phận thực hiện đồng thời:

Phương pháp cũ

↓

Excel / Google Sheet

↓

Đối chiếu

↓

Phần mềm Quản lý Sản xuất Nhà máy

### **Hỗ trợ triển khai**

* Hotfix: Khắc phục ngay lập tức một lỗi nghiêm trọng đang ảnh hưởng đến sản xuất

* Debug, fix bug: Tìm kiếm, xác định nguyên nhân sửa các lỗi, sự cố hoặc hỏng hóc của phần mềm. Đảm bảo phần mềm hoạt động ổn định

* Hỗ trợ người dùng

## **Tuần 3–4 (15/08 – 31/08)**

### **Chạy thực tế và đối soát dữ liệu**

Chạy thực tế và đối chiếu dữ liệu giữa Excel/Google Sheet và phần mềm.

Bao gồm:

### **Kế hoạch sản xuất**

* Đơn hàng

* Kế hoạch sản xuất/LSX

* Tiến độ

### **BOM**

* Định mức

* Tỷ lệ phối trộn thực tế

### **Kho**

* Tồn đầu kỳ

* Nhập

* Xuất

* Tồn cuối kỳ

### **Nguyên vật liệu**

* Tồn đầu ca

* Cấp phát

* Tiêu hao thực; tiêu hao định mức

* Tồn cuối ca

### **Sản xuất**

* Sản lượng

* Thành phẩm

* Bán thành phẩm

* Phế phẩm

### **Thống kê & QC**

* Tỷ lệ đạt

* Tỷ lệ lỗi, phế, hỏng, hao hụt

* Hiệu suất ca

### **Song song Phòng IT thực hiện**

* Optimize code: Tối ưu hóa phần mềm nhằm tăng tốc độ xử lý, trải nghiệm của người dùng

  * Tối ưu Database

  * Tối ưu API

  * Tinh chỉnh UI/UX

  * Cải thiện tốc độ xử lý

* Hoàn thiện báo cáo

* Bổ sung chức năng theo góp ý

## ***b. Tháng 09/2026***

Tiếp tục Pilot thực tế.

### **Chạy song song**

* Trong toàn bộ tháng 09, chạy song song và tiếp tục theo dõi, đối chiếu kết quả tại Nhà máy Đà Nẵng, Phú Thọ. Xử lý dứt điểm các sai lệch, chuẩn hóa dữ liệu và luồng nghiệp vụ.

* Phòng IT tiếp tục hỗ trợ các bộ phận triển khai triển khai song song, khóa việc sửa tính năng (chỉ tập trung cho hệ thống hoạt động ổn định, không thêm tính năng mới), đóng gói phiên bản phần mềm gần chính thức Release Candidate (RC)

* *(Trong thời gian này Phòng IT gối đầu triển khai dự án cấp thiết: Nhân sự, Điều hành xe, Số hóa kho, Đồng bộ dữ liệu Kế toán AMIS)*

### **Hoàn thiện hệ thống**

Trong tháng 09:

* Khóa thay đổi chức năng lớn

* Chỉ sửa lỗi

* Tối ưu hiệu năng

* Chuẩn hóa dữ liệu

* Đóng gói thành bản gần chính thức Release Candidate (RC)

### **Cuối tháng 09**

### **Nghiệm thu Pilot**

Đánh giá:

* Độ chính xác dữ liệu

* Độ ổn định hệ thống

* Hiệu năng

* Khả năng đáp ứng nghiệp vụ

Nếu:

* Độ chính xác ≥ 98%

* Hệ thống vận hành ổn định

* Người thao tác (công nhân, quản đốc, thống kê & QC, kho) chấp nhận

→ Chuyển sang Go-Live.

# **3\. Giai đoạn 3 – Go-Live toàn Tập đoàn (Tháng 10–12/2026)**

## ***a. Tháng 10-11/2026 – Go-Live đồng thời toàn Tập đoàn***

### **Phạm vi triển khai**

Triển khai chính thức đồng thời tại tất cả các nhà máy của Tập đoàn:

* Nhà máy Hà Nội

* Nhà máy Đà Nẵng

* Nhà máy Phú Thọ

* Nhà máy Đà Nẵng

* Nhà máy Miền Nam

### **Nội dung triển khai**

* Cài đặt hệ thống, chuẩn hóa dữ liệu Master Data cho từng Nhà máy, hướng dẫn đào tạo các bộ phận thao tác.

* Chính thức đưa hệ thống vào vận hành.

* Chuyển toàn bộ nghiệp vụ sản xuất sang phần mềm mới.

* Theo dõi dữ liệu sản xuất theo thời gian thực.

* Hỗ trợ trực tiếp tại các nhà máy trong thời gian đầu vận hành.

* Hỗ trợ từ xa thông qua hệ thống báo lỗi/tester và Hotline.

* Kiểm tra báo cáo điều hành và các chỉ số KPI sản xuất.

* Theo dõi các cảnh báo tồn kho, tiêu hao nguyên vật liệu, tiến độ lệnh sản xuất và chất lượng sản phẩm.

### **Hỗ trợ sau Go-Live**

Trong 30 ngày đầu sau Go-Live:

* Theo dõi hoạt động của hệ thống hằng ngày.

* Hotfix các lỗi phát sinh nếu có.

* Tối ưu hiệu năng Database và API.

* Điều chỉnh giao diện và quy trình theo thực tế sử dụng (không thay đổi nghiệp vụ cốt lõi).

* Hỗ trợ người dùng xử lý các tình huống vận hành.

## ***b. Tháng 12/2026 – Ổn định hệ thống và Nghiệm thu***

### **Đánh giá vận hành**

* Đánh giá mức độ ổn định của hệ thống.

* Đánh giá hiệu quả vận hành tại các nhà máy.

* Kiểm tra tính chính xác của số liệu sản xuất.

* Đánh giá các chỉ số KPI sản xuất và hiệu quả sử dụng hệ thống.

### **Tổng nghiệm thu dự án**

* Nghiệm thu toàn bộ các phân hệ theo phạm vi dự án.

* Bàn giao Source Code.

* Bàn giao Database.

* Bàn giao API và tài liệu tích hợp.

* Bàn giao tài liệu hướng dẫn sử dụng và tài liệu kỹ thuật.

* Bàn giao tài khoản quản trị hệ thống.

* Chuyển sang giai đoạn bảo hành, bảo trì và nâng cấp.

### **Phiên bản bàn giao**

* Phần mềm chính thức Quản lý Nhà máy Sản xuất của Tập đoàn Việt Nhật

* Bộ video hướng dẫn thao tác cho từng nhóm đối tượng

* Tài liệu sử dụng 

# **4\. Giai đoạn 4 – Vận hành và nâng cấp (Từ 01/01/2027)**

Sau khi Go-Live, hệ thống chuyển sang giai đoạn vận hành ổn định kết hợp bảo trì và nâng cấp định kỳ.

| Chu kỳ | Nội dung |
| ----- | ----- |
| Quý I/2027 | Tối ưu hiệu năng, cập nhật giao diện, báo cáo, tối ưu Database |
| Quý II/2027 | Nâng cấp BOM, Kế hoạch sản xuất, Dashboard quản trị |
| Quý III/2027 | Nâng cấp UI/UX, tối ưu API, bổ sung báo cáo |
| Quý IV/2027 | Đánh giá toàn hệ thống, lập kế hoạch Version 2.0 |

## **Công việc định kỳ**

* Kiểm tra Database

* Kiểm tra Backup

* Kiểm tra Log

* Kiểm tra hiệu năng Server

* Tối ưu API

* Tối ưu Dashboard

* Vá lỗi bảo mật

* Cập nhật thư viện

* Bổ sung các báo cáo quản trị

* Kiểm tra cơ chế Backup & Disaster Recovery, đảm bảo hệ thống luôn live

Từ 01/01/2027: Hệ thống vận hành ổn định, thực hiện bảo trì và nâng cấp định kỳ theo chu kỳ 3 tháng/lần, bổ sung các chức năng mới, tối ưu hiệu năng, mở rộng tích hợp với các hệ thống ERP, Kế toán, IoT và thiết bị sản xuất khi có nhu cầu thành các phiên bản Version 2.0; Version 3.0.

[image1]: <data:image/png;base64,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23sBErgRoI4vntwxhsRFTqeffvqaspzTXXfdteZX5hAkcPEoF8chgStHqh1beeFtQMCmTZsmj3bEyj7niBnFzY6oQZZSt/wAlD/A5fbWH/zHBooUD7G2CRxFDOvg/6W5fWwLz7ncvh+7Pb7/LufZSeBGgDq+eGqLcWrHHCsSuHiUi+OQwJUj1Y796FMUe/fu9UWDidhmF1L9hASuIOr44qktxqkdc6xI4OJRLo5DAleOVDsuJXDLRKqfkMAVRB1fPLXFOLVjjhUJXDzKxXFI4MqRasc4XKip/zQNCVxB1PHFU1uMJXDCo1wchwSuHGrH8UjgCqKOL57aYiyBEx7l4jgkcOVQO45HAlcQdXzx1BZjCZzwKBfHIYErh9pxPBK4gqjji6e2GEvghEe5OA4JXDnUjuORwBVEHV88tcVYAic8ysVxSODKoXYcjwSuIOr44qktxhI44VEujkMCVw6143gkcAVRxxdPbTGWwAmPcnEcErhyqB3HI4EriDq+eGqL8XnnneeLRo0ELh7l4jgkcOVQO45HAlcQdXzx1Bbjc8891xeNGglcPMrFcUjgyqF2HI8EriDq+OKpLcZnn322Lxo1Erh4lIvjkMCVQ+04HglcQdTxxVNbjJ/znOf4olEjgYtHuTgOCVw51I7jkcAVRB1fPLXF+PTTT/dFo0YCF49ycRwSuHKoHccjgSuIOr54aonxkUceOelEjjnmmObxj3988573vMdXGSUSuHiUi+OQwJVD7TgeCVxB1PHFU0uMr7322ubwww9vDj744GbDhg1+8WiRwMWjXByHBK4casfxSOAKoo4vnppifM0110zkbdOmTX7RaJHAxaNcHIcErhxqx/FI4Aqiji+e2mJ8yCGH+KJRI4GLR7k4DglcOdSO45HAFUQdXzxjjvFdd93VvOtd72ouvfTSye1DTjvttObEE09sTjnllOYf/aN/1Lz+9a9v3v72tzf//b//d7/qaJDAxaNcHIcErhxqx/FI4Aqiji+escT405/+dHPSSSc127Ztaz7ykY809913n6/SysMPP9zs3r27OfbYY5u/83f+TnPdddf5KgtBAhePcnEcErhyqB3HI4EriDq+eBYdY4yeXX755c2pp57a3HzzzX7xXED+zj///OYFL3hB853vfMcvLooELh7l4jjmEbgtW7ZMnTZu3LimbFmmts/28z//8z5E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>

[image2]: <data:image/png;base64,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>