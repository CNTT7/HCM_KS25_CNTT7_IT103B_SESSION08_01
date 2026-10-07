Phân tích lỗi & Lập bảng Test Cases (trình bày trong README.md):
Đọc hiểu mã nguồn, xác định dòng lệnh sai logic và phân tích nguyên nhân kỹ thuật dẫn đến sự cố nghiệp vụ.
- sử dụng pop thay vì shift nên không hợp lý -> xe đến sau sạc trước.
- điều kiện trong mảng sai dẫn đến kết quả không mong muốn.

Lập bảng 02 Test Cases đối chứng gồm các cột: Trường hợp kiểm thử, Dữ liệu đầu vào, Kết quả sai thực tế, Kết quả đúng mong đợi.

Trường hợp kiểm thử: Theo đề cho 
Dữ liệu đầu vào: 
const fastChargingRate = 4500;
const waitingQueue = ['29A-112.33', '30E-889.12', '51K-678.99'];
Kết quả sai thực tế: 
Xe được điều phối vào sạc: 51K-678.99
solution_ex1.js:15 Tổng sản lượng: NaN kWh
solution_ex1.js:16 Tổng doanh thu: NaN VNĐ

Kết quả đúng mong đợi: 
Xe được điều phối vào sạc: 29A-112.33
solution_ex1.js:15 Tổng sản lượng: 166.5 kWh
solution_ex1.js:16 Tổng doanh thu: 749250 VNĐ

Trường hợp kiểm thử: cho 10 chiếc xe vào 
Dữ liệu đầu vào: 
const fastChargingRate = 4500;
const waitingQueue = [
  '29A-112.33', 
  '30E-889.12', 
  '51K-678.99',
  '86A-224.56',
  '59G-777.88',
  '43C-123.45',
  '15A-456.78',
  '65B-987.65',
  '36C-332.11',
  '92A-555.22'
];
Kết quả sai thực tế: 
Xe được điều phối vào sạc: 92A-555.22
solution_ex1.js:26 Tổng sản lượng: NaN kWh
solution_ex1.js:27 Tổng doanh thu: NaN VNĐ

Kết quả đúng mong đợi: 
Xe được điều phối vào sạc: 29A-112.33
solution_ex1.js:26 Tổng sản lượng: 166.5 kWh
solution_ex1.js:27 Tổng doanh thu: 749250 VNĐ