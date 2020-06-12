 # Chức năng /BaoCaoTongHopTinhHinhDieuTriNoiTru

## Chức năng chung

Khởi tạo quản lý hồ bệnh án ngoại trú

Khởi tạo quản lý vỏ bệnh án ngoại trú

Nhập thông tin khám bệnh theo phiếu điều trị

Hướng giải quyết: Xuất viện chuyển tuyến chuyển phòng, ...

In ấn các mẫu phiếu phục vụ công tác khám chữa bệnh tại đơn vị

# Cấu hình thay đổi

## In phiếu điều trị BANT

Mô tả chi tiết chức năng

	In phiếu điều trị BANT

Mục đích áp dụng chức năng

	In phiếu điều trị cho bệnh nhân khám bệnh án ngoại trú

Cấu hình tham số

	chưa có

Cấu hình report mẫu

	82047: Mẫu tổng hợp tiêu đề lập lại PDF. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoTongHopTinhHinhDieuTriNoiTru.jasper"

    82048: Mẫu tổng hợp tiêu đề không lập lại PDF. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoTongHopTinhHinhDieuTriNoiTruNotRepeatHeader.jasper"

	82049: Mẫu tổng hợp XLSX. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoTongHopTinhHinhDieuTriNoiTru.jasper"

	82053: Mẫu chi tiết tiêu đề lập lại PDF. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoChiTietTinhHinhDieuTriNoiTru.jasper"

	82054: Mẫu chi tiết tiêu đề không lập lại PDF. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoChiTietTinhHinhDieuTriNoiTruNotRepeatHeader.jasper"

	82055: Mẫu chi tiết XLSX. Đường dẫn mặc định "/WEB-INF/pages/BaoCaoNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTru/BaoCaoTongHopTinhHinhDieuTriNoiTruReports/BaoCaoChiTietTinhHinhDieuTriNoiTru.jasper"
<a href="https://imgur.com/yvrCnOR"><img src="https://i.imgur.com/yvrCnOR.png" title="source: imgur.com" /></a>

Hướng dẫn thao tác

	Bước 1: vào link chức năng: BaoCaoTongHopTinhHinhDieuTriNoiTru
	Bước 2: Chọn ngày để lấy báo cáo
	Bước 3: Chọn mẫu loại tập tin để lấy báo cáo.
	Bước 4: Nếu chọn loại tập tin là PDF, bạn cần chọn loại mẫu báo cáo là lập lại tiêu để hoặc bỏ check để loại không lập lại tiêu đề. Nếu chọn loại tập tin là XSLX thì không cần quan tâm đến lựa chọn này.
	Bước 5: Nếu muốn lấy dữ liệu xuất báo cáo với mẫu tổng hợp, người dùng thực hiện click vào nút "Báo cáo tổng hợp", ngược lại nếu muốn lựa chọn mẫu chi tiết click vào nút "Báo cáo chi tiết".
	Bước 6: hệ thống trả về tập tin theo lựa chọn chứa thông tin báo cáo. Người dùng cần thực hiện kiểm tra dữ liệu trong tập tin.

> Lưu ý có thông nhất công thức của 2 cột "Bệnh nhân dịch vụ" và cột "Còn lại": BN cũ + Vào viện – Chuyển tuyến – Chuyển khoa đi + Chuyển khoa đến – Tử vong - Xuất viện - Kết thúc đợt điều trị

Cách lấy số liệu
| STT | Cột  | Mô tả |
| -- | -- | -- |
| 1 | BN cũ | Số lượng BN đang điều trị (chưa xuất viện, chuyển khoa) [tới 23:59 ngày kiểm tra  - 1] // Mới vào khoa, 1 điều trị có giường, 2 điều trị không giường : ngay_nhapvien < NgàyKT // 3 xuất viện, 4 chuyển viện, 5 tử vong, 6 trốn viện : ngay_nhapvien < NgàyKT và ngayravien > NgàyKT |
| 2 | Vào viện | Số lượng BN nhập viện từ 00:00 đến 23:59 ngày kiểm tra //	mới vào khoa, 1 điều trị có giường, 2 điều trị không giường : ngay_nhapvien = NgàyKT //	3 xuất viện, 4 chuyển viện, 5 tử vong, 6 trốn viện : ngay_nhapvien = NgàyKT |
| 3 | Xuất viện | Số lượng BN xuất viện từ 00:00 đến 23:59 ngày kiểm tra: 3 xuất viện: ngay_ra = NgàyKT |
| 4 | Chuyển tuyến | Số lượng BN chuyển tuyến từ 00:00 đến 23:59 ngày kiểm tra: 4 chuyển viện: ngay_ra = NgàyKT |
| 5 | Tử vong | Số lượng BN tử vong từ 00:00 đến 23:59 ngày kiểm tra //	5 tử vong: ngay_ra = NgàyKT |
| 6 | Chuyển khoa đi | Số lượng BN chuyển khoa đi từ 00:00 đến 23:59 ngày kiểm tra // 8 chuyển khoa đi: ngay_chuyendi= NgàyKT |
| 7 | Chuyển khoa đến | Số lượng BN chuyển khoa đến từ 00:00 đến 23:59 ngày kiểm tra // chuyển khoa đến: ngay_chuyenden= NgàyKT |
| 8 | BN dich vụ | Số BN dịch vụ : Số BN dịch vụ đang điều trị: Không bảo hiểm // (BN cũ + Vào viện – Chuyển tuyến – Chuyển khoa đi + Chuyển khoa đến – Tử vong) |
| 9 | Còn lại( điều chỉnh lại để lấy được số liệu chính xác) | Còn lại: BN cũ + Vào viện – Chuyển tuyến – Chuyển khoa đi + Chuyển khoa đến – Tử vong - Xuất viện - Kết thúc đợt điều trị |

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
| https://cntt.vnpt.vn/browse/TGGDEV-71856 | 11/06/2020 | develop | HNI |