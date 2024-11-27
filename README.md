# Phân Tích Phân Khúc Khách Hàng Chiến Dịch Marketing Của IFood (2012-2014)

## Mục lục

- [Tổng quan dự án](#tổng-quan-dự-án)
- [Mục tiêu](#mục-tiêu)
- [Dữ liệu](#dữ-liệu)
- [Phương pháp phân tích dữ liệu](#phương-pháp-phân-tích-dữ-liệu)
- [Insights](#insights)

### Tổng quan dự án

IFood là nền tảng đặt đồ ăn online hàng đầu tại Brazil và phục vụ gần một triệu hành khách một năm. Danh mục sản phẩm của iFood đa dạng, bao gồm: rượu, các sản phẩm làm từ thịt, trái cây, cá và đồ ngọt. Khách hàng có thể đặt hàng thông qua 3 kênh: cửa hàng vật lý, catalog và website của công ty. Xét ở phương diện toàn cầu, iFood có lượng doanh thu ổn định trong suốt 3 năm qua, tuy nhiên, tăng trưởng lợi nhuận trong 3 năm tới không có nhiều kì vọng. Vậy nên, dự án này sẽ nhằm cải thiện hiệu quả các hoạt động marketing, bằng cách phân tích dữ liệu từ các chiến dịch trong quá khứ và xác định chiến lược phù hợp cho các chiến dịch trong tương lai.

Chiến dịch thứ 6 (sắp tới) của iFood hướng đến việc ra mắt sản phẩm mới. 1 cuộc khảo sát đã được tiến hành trên 2.240 khách hàng thông qua điện thoại. 

### Mục tiêu

Mục tiêu của dự án là phân tích đặc điểm hành vi khách hàng sẵn sàng mua sản phẩm mới.

Mục tiêu cụ thể được giải đáp thông qua những câu hỏi sau:
- Những chiến dịch trước đó có sự khác biệt nhiều về khách hàng so với chiến dịch thứ 6 không?
- Đặc điểm về nhân khẩu học và hành vi của tệp khách hàng tiềm năng là gì?

### Dữ liệu

Dữ liệu được cung cấp bởi công ty iFood, bao gồm các nội dung sau:
- Số lượng chiến dịch thành công
- Thông tin nhân khẩu học về khách hàng: thu nhập, giới tính... và hành vi mua như lần mua gần đây nhất, số lượt ghé trang web 1 tháng...
- Thông tin về giá trị giao dịch với các sản phẩm ứng với mỗi khách hàng

### Phương pháp phân tích dữ liệu

Xem thêm tại file [xử lý và phân tích dữ liệu](https://github.com/nhungnguyen1111/Customer_Segmentation_Analysis/blob/256484406c697dba8c071bc9d92e887fd8a3fdd9/data%20transforming%20%26%20data%20analysis.md)

### Insights 

Vì tỷ lệ thành công ở chiến dịch cuối đạt mức 14,93%, cao hơn hẳn so với những chiến dịch trước đó nên đặc điểm về nhân khẩu học của khách hàng mục tiêu được rút ra từ chiến dịch này. Và đặc điểm hành vi sẽ được rút ra từ dữ liệu quá khứ trong 2 năm qua (2012 - 2014).

![](https://i.imgur.com/F1AirQg.png)

#### Nhân khẩu học

Khách hàng mục tiêu của chiến dịch sắp tới là tệp khách hàng trưởng thành, có thu nhập từ trung bình đến cao, cụ thể là:

- Độ tuổi: từ 25 đến 64 tuổi
- Học vấn: tối thiểu từ Đại học trở lên
- Thu nhập hàng năm: từ R$ 20K đến R$ 80K

![](https://i.imgur.com/7O3gjRk.png)

#### Hành vi

Kênh mua sắm chiếm đa số là cửa hàng vật lý. Mặc dù iFood bắt nguồn từ nền tảng online nhưng số lượng giao dịch chủ yếu đến từ kênh bán hàng offline, điều này cho thấy iFood đã kết hợp mô hình hybrid: bao gồm cửa hàng và online.

=> **Đề xuất**: Chiến dịch sắp tới có thể tận dụng kênh phân phối này như sau:

- Kênh bán hàng offline: tiếp cận tệp đối tượng khách hàng ở các thành phố có mật độ dân cư đông đúc, cụ thể là ở các cửa hàng của iFood có lượng khách lớn.
- Kênh online: Điểm mạnh của kênh này là thu hút được lượng khách hàng nhiều hơn nhưng với danh mục sản phẩm của iFood là rượu, thịt, cá..., mua sắm online gặp cản trở là thiếu thông tin về sản phẩm và giải đáp từ nhân viên. Do đó, website và catalog cần nêu rõ thông tin chi tiết về sản phẩm (ví dụ như tên hãng rượu, khối lượng, tên phần thịt...) và hotline hỗ trợ của chính iFood và các nhà hàng liên quan.

![](https://i.imgur.com/8i0idHJ.png)

Qua phân tích RFM cho thấy khoảng thời gian từ lần cuối khách hàng mua cho đến hiện tại trung bình là 49 ngày và giá trị trung bình cho mỗi giao dịch là R$ 592. Đối với các loại thực phẩm như thịt, cá thì con số 49 ngày vẫn còn khá dài và cần thu hẹp.

Tổng hợp dữ liệu từ 5 chiến dịch trước cho thấy 3 nhóm khách hàng chiếm tỷ lệ cao lần lượt là: Champion (23,16%), Can't Lose Them (22,57%) và Potential Loyalist (21,37%); những nhóm còn lại đều dưới 12%. Điều này cho thấy tệp khách hàng hiện tại của iFood chủ yếu là nhóm khách hàng trung thành có mức độ chi tiêu cao. Tuy nhiên, riêng với nhóm Can't Lose Them khi không có giao dịch nào xảy ra gần đây phản ánh rằng iFood cần có những hoạt động cụ thể như nhắn tin hoặc gửi email hỏi thăm khách hàng. 

Chiến dịch sắp tới cần tập trung vào 3 nhóm này trước và đồng thời thiết lập chiến lược quản trị khách hàng dài hạn cho từng nhóm khách hàng.

![](https://i.imgur.com/Ngoynz7.png)
