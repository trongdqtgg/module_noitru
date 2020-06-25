#  Báo cáo công tác chuyển tuyến

## Link chức năng

	/baocaocongtacchuyentuyen

## Mô tả chung

	Báo cáo dùng để thống kê số lượng người bệnh chuyển tuyến đi và chuyển tuyến đến của đơn vi.


## Mẫu report 
<a href="https://imgur.com/kDKb9wv"><img src="https://i.imgur.com/kDKb9wv.png" title="source: imgur.com" /></a>


# Chức năng điều chỉnh

## Trống nơi chuyển đến
	- EHEALTH kiểm tra hiện tại đơn vị đang bật tham số 82119 = 1 (Báo cáo công tác chuyển tuyến lấy thông tin từ đơn vị chuyển)

	- Ý nghĩa của tham số nếu đơn vị này có chuyển tuyến đi đến một bệnh viện khác mà bệnh viện đó có tiếp nhận BN thì sẽ lấy vào báo cáo, Tên đơn vị chuyển đến sẽ lấy thông tin Tên nơi giới thiệu được nhập lúc tiếp nhận BN, tuy nhiên có nhiều trường hợp BV tiếp nhận BN chuyển từ nơi khác nhưng không nhập thông tin ô Tên nơi giới thiệu nên vào báo cáo bị trống Tên nơi chuyển đến
	
	- EHEALTH đã kiểm tra và điều chỉnh lại, thêm giá trị tham số 82119  = 3, đối với các BN tiếp nhận không nhập ô Tên nơi giới thiệu sẽ lấy Tên đơn vị đã thao tác chuyển tuyến cho BN làm tên nơi chuyển đến trong báo cáo, hiện tại Số liệu BN chuyển đến vẫn giữ nguyên và không còn trống cột Tên nơi chuyển đến

	Yêu cầu thay đổi

	| Mã yêu cầu | Ngày thay đổi  | Release | Tỉnh đang sử dụng |
	| -- | -- | -- | -- |
	| https://cntt.vnpt.vn/browse/EHEALTHCR-22163 |  |  |  |
		
