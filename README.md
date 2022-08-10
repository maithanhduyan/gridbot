# gridbot
Automation Trading by Grid

### Giới Thiệu

GridBot là gì ?
Hệ thống giao dịch tự động dựa trên cài đặt giá của người dùng.
Gồm 3 đầu vào: giá cao nhất, giá thấp nhất, số lượng lệnh(số chẵn).
Hệ thống tự động tính toán số lượng lưới và đặt lệnh sẵn.

Nguồn tham khảo: bitsgap.com 

Cơ chế hoạt động của GridBot
Mua thấp bán cao
Khối lượng giao dịch như nhau. Được tính tại thời điểm setup khi người dùng chọn giá trần, giá sàn, số lượng lưới, vốn ban đầu.
Ví dụ: 
Vốn tối thiểu là 500.000 VND. 
Mã tài sản ABC/VND đang có giá 50000 VNĐ

Người dùng sử dụng lưới với các thông số sau:
	Giá trần là: 60000 VND
	Giá sàn là:  40000 VND
	Số lượng lưới là: 10
Hệ thống sẽ đặt: 
5 lệnh mua vào với giá: 40K, 42K, 44K, 46K, 48K
5 lệnh bán ra với giá : 52K, 54K, 56K, 58K, 60K 
		Khối lượng giao dịch cùng là 1 đơn vị.
	Vận hành: 
		Mua trước 5 đơn vị ACB với giá hiện tại 50K.
		Trường hợp giá lên:
			Khớp lệnh với giá 52K → Bán ra
			Hệ thống tự đặt lệnh mua vào giá 50K→ Mua vào
		Trường hợp giá xuống:
			Khớp lệnh với giá 48K → Mua vào
			Hệ thống tự đặt lệnh bán ra với giá 50K → Bán ra

			
	
Yêu cầu Project
OS: Windows Server
Editor: VSCode
Backend: NodeJS
Fontend: HTML, CSS, Javascript, Bootstrap, Lightweight Charts
Extension API: CCXT
Sàn giao dịch mặc định: Binance Exchange
Testing: BTC/USD

Thông tin Project
	Mã nguồn: https://github.com/maithanhduyan/gridbot