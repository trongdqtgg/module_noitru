 # Chức năng /khambenhnoitru

## Chức năng chung

Khởi tạo quản lý hồ bệnh án nội trú

Khởi tạo quản lý vỏ bệnh án chuyên khoa

Nhập thông tin khám bệnh theo phiếu điều trị

Hướng giải quyết: Xuất viện chuyển tuyến chuyển phòng, ...

In ấn các mẫu phiếu phục vụ công tác khám chữa bệnh tại đơn vị

# Cấu hình thay đổi

## Nhập cân nặng cho thẻ TE dưới 1 tuổi chỉ cần nhập cân nặng ở phiếu vào viện khi nhập viện

Mô tả chi tiết chức năng

	Lấy được cân nặng của thẻ TE

Mục đích áp dụng chức năng

	Theo yêu cầu của đơn vi

Cấu hình tham số

	Set 31701227608  = 1

Cấu hình report mẫu

	Sử dụng rp hiện tại của đơn vị, không cần cấu hình

Hướng dẫn thao tác

	Bước 1: Vào nội trú -> Tiếp nhận nội trú -> Nhập bệnh nhân ->Tạo phiếu khám bệnh

	Bước 2: Nhập các thông tin khám chữa bệnh

	Bước 3 : Vào nội trú Chọn bệnh nhân, chuột phải vào phiếu điều trị, chọn lấy dữ liệu phiếu KB

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
| https://cntt.vnpt.vn/browse/TGGDEV-57468 | 11/06/2020 | develop | NAN |

## Thêm giờ chỉ định vào chỉ định thủ thuật form khám bệnh BANT

Mô tả chi tiết chức năng

	Hiên được giơ trên form thủ thuật phẩu thuật của khám bệnh BANT

Mục đích áp dụng chức năng

	Theo yêu cầu của đơn vi

Cấu hình tham số

	Set 92007  = 1

Cấu hình report mẫu

	Không cấu hình rp

Hướng dẫn thao tác

	Bước 1: Vào Khám bệnh -> Khám bệnh BANT -> Chọn bệnh nhân -> Vào form TTPT

	Bước 2: Hiện thị được giờ

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
|  |  |  |  |

## Chỉnh sửa rp phiếu truyền dịch hiển thị mã bệnh phụ

Mô tả chi tiết chức năng

	Lấy được bệnh phụ khi in ra report

Mục đích áp dụng chức năng

	Theo yêu cầu của đơn vi

Cấu hình tham số

	Không cần cấu hình

Cấu hình report mẫu

	In report không cân cấu hình

Hướng dẫn thao tác

	Vào Khám bệnh --> Khám bệnh nội trú --> Chọn bệnh nhân --> Hồ sơ khám --> Phiếu dịch truyền --> In phiếu

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
|  |  |  |  |

## Chỉnh sửa rp tạo nhiều phiếu chăm sóc có hiển thị mã bệnh phụ

Mô tả chi tiết chức năng

	Lấy được bệnh phụ khi in ra report

Mục đích áp dụng chức năng

	Theo yêu cầu của đơn vi

Cấu hình tham số

	Không cần cấu hình

Cấu hình report mẫu

	In report không cân cấu hình

Hướng dẫn thao tác

	Vào Khám bệnh --> Khám bệnh nội trú --> Chọn bệnh nhân --> Chọn phiếu điều trị --> Phiếu chăm sóc --> In phiếu

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
|  |  |  |  |

## Thêm mẫu báo cáo 14 vào báo cáo Thống kê bệnh tật theo ICD 10

Mô tả chi tiết chức năng

	Thêm cột mới theo mẫu của Bộ
	
Mục đích áp dụng chức năng

	Cập nhật theo mẫu của Bộ

Cấu hình tham số

	69116 = 1

Cấu hình report mẫu

	In report không cân cấu hình

Hướng dẫn thao tác

	Vào Báo cáo --> Thống kê bệnh tật theo ICD 10

	Thực hiện thao tác chọn khoảng thời gian để in ra báo cáo

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
|  |  |  |  |

## Cảnh báo lấy dữ liệu thuốc ngoại trú của bệnh nhân nội trú (Nếu có)

Mô tả chi tiết chức năng

	Nếu BN chưa được lấy dữ liệu từ ngoại trú vào nội trú thì khi lưu tờ điều trị sẽ xuất hiện cảnh báo
	
Mục đích áp dụng chức năng

	Chức năng riêng của NAN lưu ý khi sử dụng. Mục đích đơn vị quên lấy dữ liệu từ ngoại trú

Cấu hình tham số

	40095 - Cảnh báo lấy dữ liệu thuốc từ ngoại trú = 1

	40096 - Cảnh báo lấy dữ liệu thuốc từ ngoại trú = 3

Cấu hình report mẫu

	In report không cần cấu hình

Hướng dẫn thao tác

	Vào tiepnhanbenhnhan --> Thực hiện chỉ định thuốc, cận lâm sàng --> Nhập viện

	Nếu BN chưa được lấy dữ liệu từ ngoại trú vào nội trú thì khi lưu tờ điều trị sẽ xuất hiện cảnh báo

<a href="https://imgur.com/mB2KEr3"><img src="https://i.imgur.com/mB2KEr3.png" title="source: imgur.com" /></a>

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
| https://cntt.vnpt.vn/browse/TGGDEV-64389 | 11/06/2020 | Develop | NAN |

## Điều chỉnh in toa thuốc đông y nội trú

Mô tả chi tiết chức năng

	1. Điều chỉnh chữ than hiếu chữ g

    2. Thang thuốc có 3 thang nhưng khi bấm in ra thì thiếu số Gam nhân với số thang ra tổng Số lượng
	
Mục đích áp dụng chức năng

	In toa thuốc đông y nội trú

Cấu hình tham số

	40095 - Cảnh báo lấy dữ liệu thuốc từ ngoại trú = 1

	40096 - Cảnh báo lấy dữ liệu thuốc từ ngoại trú = 3

Cấu hình report mẫu

	89044: /WEB-INF/pages/nghean/rp_noitru_toadongy_thangthuoc.jasper

Hướng dẫn thao tác

	Vào khambenhnoitru --> Kê tab toa đông y --> In toa thuốc

<a href="https://imgur.com/G5pu2K2"><img src="https://i.imgur.com/G5pu2K2.png" title="source: imgur.com" /></a>

Yêu cầu thay đổi

| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
| -- | -- | -- | -- |
| https://cntt.vnpt.vn/browse/TGGDEV-61142 | 11/06/2020 | Develop | NAN |

